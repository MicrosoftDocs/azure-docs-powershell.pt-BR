---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261031"
---
# <span data-ttu-id="ca0c6-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="ca0c6-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="ca0c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0c6-103">Test-AzStackHCIConnection verifica a conectividade de nós clusterizados locais para os serviços do Azure exigida pela HCI de pilha do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="ca0c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca0c6-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="ca0c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca0c6-105">DESCRIPTION</span></span>
<span data-ttu-id="ca0c6-106">Test-AzStackHCIConnection verifica a conectividade de nós clusterizados locais para os serviços do Azure exigida pela HCI de pilha do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="ca0c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca0c6-107">EXAMPLES</span></span>

### <span data-ttu-id="ca0c6-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="ca0c6-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node. Success case.
```

<span data-ttu-id="ca0c6-109">\>Teste C:\PS-AzStackHCIConnection: conecta-se ao serviço de HCI de pilha do Azure EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: resultado real: êxito</span><span class="sxs-lookup"><span data-stu-id="ca0c6-109">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span></span>

### <span data-ttu-id="ca0c6-110">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="ca0c6-110">EXAMPLE 2</span></span>
```
Invoking on one of the cluster node. Failed case.
```

<span data-ttu-id="ca0c6-111">\>Teste C:\PS-AzStackHCIConnection: conecta-se ao serviço HCI de pilha do Azure EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: resultado verdadeiro: falha FailedNodes: Node1inClus2, Node2inClus3</span><span class="sxs-lookup"><span data-stu-id="ca0c6-111">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span></span>

## <span data-ttu-id="ca0c6-112">OS</span><span class="sxs-lookup"><span data-stu-id="ca0c6-112">PARAMETERS</span></span>

### <span data-ttu-id="ca0c6-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ca0c6-113">-ComputerName</span></span>
<span data-ttu-id="ca0c6-114">Especifica um dos nós do cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-114">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="ca0c6-115">-Credential</span></span>
<span data-ttu-id="ca0c6-116">Especifica a credencial para o ComputerName.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-116">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="ca0c6-117">Padrão é o usuário atual que está executando o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-117">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-118">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="ca0c6-118">-EnvironmentName</span></span>
<span data-ttu-id="ca0c6-119">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-119">Specifies the Azure Environment.</span></span>
<span data-ttu-id="ca0c6-120">O padrão é AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-120">Default is AzureCloud.</span></span>
<span data-ttu-id="ca0c6-121">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="ca0c6-121">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-122">-Região</span><span class="sxs-lookup"><span data-stu-id="ca0c6-122">-Region</span></span>
<span data-ttu-id="ca0c6-123">Especifica a região à qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-123">Specifies the Region to connect to.</span></span>
<span data-ttu-id="ca0c6-124">Não usado, a menos que seja Canárias região.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-124">Not used unless it is Canary region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0c6-125">CommonParameters</span></span>
<span data-ttu-id="ca0c6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0c6-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca0c6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0c6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca0c6-128">INPUTS</span></span>

## <span data-ttu-id="ca0c6-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca0c6-129">OUTPUTS</span></span>

### <span data-ttu-id="ca0c6-130">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-130">PSCustomObject.</span></span> <span data-ttu-id="ca0c6-131">Retorna as propriedades a seguir no PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="ca0c6-131">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="ca0c6-132">Teste: nome do teste executado.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-132">Test: Name of the test performed.</span></span>
### <span data-ttu-id="ca0c6-133">EndpointTested: ponto de extremidade usado no teste.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-133">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="ca0c6-134">IsRequired: true ou false</span><span class="sxs-lookup"><span data-stu-id="ca0c6-134">IsRequired: True or False</span></span>
### <span data-ttu-id="ca0c6-135">Resultado: êxito ou falha</span><span class="sxs-lookup"><span data-stu-id="ca0c6-135">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="ca0c6-136">FailedNodes: lista de nós em que o teste falhou.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-136">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="ca0c6-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca0c6-137">NOTES</span></span>

## <span data-ttu-id="ca0c6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca0c6-138">RELATED LINKS</span></span>
