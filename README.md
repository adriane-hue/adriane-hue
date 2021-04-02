def criar_arvore_binaria(valor):
    arvore = None
    for v in valor:
        arvore = arvore_binaria_de_insercao(arvore, v)
    return arvore

def arvore_binaria_transversal(nó_arvore):
    if nó_arvore is None: return []
    else:
        esquerda, valor, direita = nó_arvore
        return (arvore_binaria_transversal(esquerda) + [valor] + arvore_binaria_transversal(direita))
