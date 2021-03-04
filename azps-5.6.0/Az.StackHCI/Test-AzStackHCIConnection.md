---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 4de1e1467e1bc422666b7144f5d5fcd6c30c0c63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888412"
---
# <span data-ttu-id="4fdd2-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="4fdd2-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="4fdd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fdd2-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdd2-103">Test-AzStackHCIConnection verifica a conectividade de nós em cluster local para os serviços do Azure exigidos pelo Azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="4fdd2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4fdd2-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="4fdd2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4fdd2-105">DESCRIPTION</span></span>
<span data-ttu-id="4fdd2-106">Test-AzStackHCIConnection verifica a conectividade de nós em cluster local para os serviços do Azure exigidos pelo Azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="4fdd2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fdd2-107">EXAMPLES</span></span>

### <span data-ttu-id="4fdd2-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="4fdd2-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="4fdd2-109">Invocando um dos nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="4fdd2-110">Caso de sucesso.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-110">Success case.</span></span>

### <span data-ttu-id="4fdd2-111">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="4fdd2-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="4fdd2-112">Invocando um dos nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="4fdd2-113">Caso com falha.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-113">Failed case.</span></span>

## <span data-ttu-id="4fdd2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4fdd2-114">PARAMETERS</span></span>

### <span data-ttu-id="4fdd2-115">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="4fdd2-115">-ComputerName</span></span>
<span data-ttu-id="4fdd2-116">Especifica um dos nós de cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="4fdd2-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="4fdd2-117">-Credential</span></span>
<span data-ttu-id="4fdd2-118">Especifica a credencial do ComputerName.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="4fdd2-119">O padrão é o usuário atual executando o Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-119">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="4fdd2-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="4fdd2-120">-EnvironmentName</span></span>
<span data-ttu-id="4fdd2-121">Especifica o Ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="4fdd2-122">O padrão é o AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-122">Default is AzureCloud.</span></span>
<span data-ttu-id="4fdd2-123">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="4fdd2-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="4fdd2-124">-Region</span><span class="sxs-lookup"><span data-stu-id="4fdd2-124">-Region</span></span>
<span data-ttu-id="4fdd2-125">Especifica a região à que se conectar.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="4fdd2-126">Não é usado, a menos que seja região canária.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-126">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="4fdd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdd2-127">CommonParameters</span></span>
<span data-ttu-id="4fdd2-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdd2-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fdd2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdd2-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fdd2-130">INPUTS</span></span>

## <span data-ttu-id="4fdd2-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4fdd2-131">OUTPUTS</span></span>

### <span data-ttu-id="4fdd2-132">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-132">PSCustomObject.</span></span> <span data-ttu-id="4fdd2-133">Retorna propriedades a seguir em PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="4fdd2-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="4fdd2-134">Teste: nome do teste executado.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="4fdd2-135">EndpointTested: Ponto de extremidade usado no teste.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="4fdd2-136">IsRequired: True ou False</span><span class="sxs-lookup"><span data-stu-id="4fdd2-136">IsRequired: True or False</span></span>
### <span data-ttu-id="4fdd2-137">Resultado: bem-sucedido ou com falha</span><span class="sxs-lookup"><span data-stu-id="4fdd2-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="4fdd2-138">FailedNodes: lista de nós nos quais o teste falhou.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="4fdd2-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="4fdd2-139">NOTES</span></span>

## <span data-ttu-id="4fdd2-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fdd2-140">RELATED LINKS</span></span>
