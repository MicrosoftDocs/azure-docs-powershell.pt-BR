---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111283"
---
# <span data-ttu-id="83d3b-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="83d3b-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="83d3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="83d3b-103">Test-AzStackHCIConnection verifica a conectividade de nós clusterados locais para os serviços do Azure exigidos pelo HCI do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="83d3b-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="83d3b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83d3b-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="83d3b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="83d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="83d3b-106">Test-AzStackHCIConnection verifica a conectividade de nós clusterados locais para os serviços do Azure exigidos pelo HCI do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="83d3b-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="83d3b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="83d3b-107">EXAMPLES</span></span>

### <span data-ttu-id="83d3b-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="83d3b-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="83d3b-109">Invoking on a of the cluster node.</span><span class="sxs-lookup"><span data-stu-id="83d3b-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="83d3b-110">Caso de sucesso.</span><span class="sxs-lookup"><span data-stu-id="83d3b-110">Success case.</span></span>

### <span data-ttu-id="83d3b-111">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="83d3b-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="83d3b-112">Invoking on a of the cluster node.</span><span class="sxs-lookup"><span data-stu-id="83d3b-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="83d3b-113">Caso com falha.</span><span class="sxs-lookup"><span data-stu-id="83d3b-113">Failed case.</span></span>

## <span data-ttu-id="83d3b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83d3b-114">PARAMETERS</span></span>

### <span data-ttu-id="83d3b-115">-NomedoCompr computador</span><span class="sxs-lookup"><span data-stu-id="83d3b-115">-ComputerName</span></span>
<span data-ttu-id="83d3b-116">Especifica um dos nó de cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="83d3b-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="83d3b-117">-Credencial</span><span class="sxs-lookup"><span data-stu-id="83d3b-117">-Credential</span></span>
<span data-ttu-id="83d3b-118">Especifica a credencial para o NomeDoCompt.</span><span class="sxs-lookup"><span data-stu-id="83d3b-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="83d3b-119">O padrão é o usuário atual executando o Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83d3b-119">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="83d3b-120">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="83d3b-120">-EnvironmentName</span></span>
<span data-ttu-id="83d3b-121">Especifica o Ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="83d3b-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="83d3b-122">O padrão é o AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="83d3b-122">Default is AzureCloud.</span></span>
<span data-ttu-id="83d3b-123">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSCloudment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="83d3b-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="83d3b-124">-Região</span><span class="sxs-lookup"><span data-stu-id="83d3b-124">-Region</span></span>
<span data-ttu-id="83d3b-125">Especifica a Região à onde se conectar.</span><span class="sxs-lookup"><span data-stu-id="83d3b-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="83d3b-126">Não é usado, a menos que seja região canária.</span><span class="sxs-lookup"><span data-stu-id="83d3b-126">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="83d3b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d3b-127">CommonParameters</span></span>
<span data-ttu-id="83d3b-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d3b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d3b-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83d3b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d3b-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="83d3b-130">INPUTS</span></span>

## <span data-ttu-id="83d3b-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="83d3b-131">OUTPUTS</span></span>

### <span data-ttu-id="83d3b-132">Pscustomobject.</span><span class="sxs-lookup"><span data-stu-id="83d3b-132">PSCustomObject.</span></span> <span data-ttu-id="83d3b-133">Retorna propriedades a seguir no PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="83d3b-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="83d3b-134">Teste: Nome do teste executado.</span><span class="sxs-lookup"><span data-stu-id="83d3b-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="83d3b-135">Ponto de Extremidade Testado: Ponto de extremidade usado no teste.</span><span class="sxs-lookup"><span data-stu-id="83d3b-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="83d3b-136">IsRequired: True or False</span><span class="sxs-lookup"><span data-stu-id="83d3b-136">IsRequired: True or False</span></span>
### <span data-ttu-id="83d3b-137">Resultado: Bem-sucedido ou Com Falha</span><span class="sxs-lookup"><span data-stu-id="83d3b-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="83d3b-138">FailedNodes: Lista de nós em que o teste falhou.</span><span class="sxs-lookup"><span data-stu-id="83d3b-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="83d3b-139">Notas</span><span class="sxs-lookup"><span data-stu-id="83d3b-139">NOTES</span></span>

## <span data-ttu-id="83d3b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83d3b-140">RELATED LINKS</span></span>
