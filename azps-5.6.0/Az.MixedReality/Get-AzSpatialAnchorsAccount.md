---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 8201780dd70c758c20660bbb8a97d358049cebf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887703"
---
# <span data-ttu-id="a286a-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a286a-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a286a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a286a-102">SYNOPSIS</span></span>
<span data-ttu-id="a286a-103">Obter Conta de Âncoras Espaciais</span><span class="sxs-lookup"><span data-stu-id="a286a-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="a286a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a286a-104">SYNTAX</span></span>

### <span data-ttu-id="a286a-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a286a-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a286a-106">GetParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a286a-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a286a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a286a-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a286a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a286a-108">DESCRIPTION</span></span>
<span data-ttu-id="a286a-109">Obter ou listar Contas de Âncoras Espaciais em determinados Grupos de Recursos e Assinaturas.</span><span class="sxs-lookup"><span data-stu-id="a286a-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="a286a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a286a-110">EXAMPLES</span></span>

### <span data-ttu-id="a286a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a286a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="a286a-112">Listar todas as Contas de Âncoras Espaciais no Grupo de Recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="a286a-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="a286a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a286a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="a286a-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span><span class="sxs-lookup"><span data-stu-id="a286a-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="a286a-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a286a-115">PARAMETERS</span></span>

### <span data-ttu-id="a286a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a286a-116">-DefaultProfile</span></span>
<span data-ttu-id="a286a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a286a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a286a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a286a-118">-Name</span></span>
<span data-ttu-id="a286a-119">Nome da conta de Âncoras Espaciais.</span><span class="sxs-lookup"><span data-stu-id="a286a-119">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a286a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a286a-120">-ResourceGroupName</span></span>
<span data-ttu-id="a286a-121">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a286a-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a286a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a286a-122">-ResourceId</span></span>
<span data-ttu-id="a286a-123">ID de Recurso da Conta de Âncoras Espaciais.</span><span class="sxs-lookup"><span data-stu-id="a286a-123">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a286a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a286a-124">CommonParameters</span></span>
<span data-ttu-id="a286a-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a286a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a286a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a286a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a286a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a286a-127">INPUTS</span></span>

### <span data-ttu-id="a286a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a286a-128">System.String</span></span>

## <span data-ttu-id="a286a-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a286a-129">OUTPUTS</span></span>

### <span data-ttu-id="a286a-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a286a-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a286a-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="a286a-131">NOTES</span></span>

## <span data-ttu-id="a286a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a286a-132">RELATED LINKS</span></span>
