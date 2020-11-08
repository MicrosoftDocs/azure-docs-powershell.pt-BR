---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2497b41399c79297726bc82e3232934cbd6768d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124558"
---
# <span data-ttu-id="14958-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="14958-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="14958-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14958-102">SYNOPSIS</span></span>
<span data-ttu-id="14958-103">Obter conta de âncoras espaciais</span><span class="sxs-lookup"><span data-stu-id="14958-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="14958-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14958-104">SYNTAX</span></span>

### <span data-ttu-id="14958-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="14958-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14958-106">Getparameterset (padrão)</span><span class="sxs-lookup"><span data-stu-id="14958-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14958-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14958-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14958-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14958-108">DESCRIPTION</span></span>
<span data-ttu-id="14958-109">Obter ou listar contas de âncora espacial em determinadas assinaturas e grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="14958-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="14958-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14958-110">EXAMPLES</span></span>

### <span data-ttu-id="14958-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14958-111">Example 1</span></span>
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

<span data-ttu-id="14958-112">Listar todas as âncoras espaciais no grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="14958-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="14958-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="14958-113">Example 2</span></span>
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

<span data-ttu-id="14958-114">Obter uma conta de âncora espacial "exemplo" no grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="14958-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="14958-115">OS</span><span class="sxs-lookup"><span data-stu-id="14958-115">PARAMETERS</span></span>

### <span data-ttu-id="14958-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14958-116">-DefaultProfile</span></span>
<span data-ttu-id="14958-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14958-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14958-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="14958-118">-Name</span></span>
<span data-ttu-id="14958-119">Nome da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="14958-119">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="14958-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14958-120">-ResourceGroupName</span></span>
<span data-ttu-id="14958-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14958-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="14958-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14958-122">-ResourceId</span></span>
<span data-ttu-id="14958-123">ID do recurso da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="14958-123">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="14958-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14958-124">CommonParameters</span></span>
<span data-ttu-id="14958-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14958-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14958-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14958-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14958-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14958-127">INPUTS</span></span>

### <span data-ttu-id="14958-128">System. String</span><span class="sxs-lookup"><span data-stu-id="14958-128">System.String</span></span>

## <span data-ttu-id="14958-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14958-129">OUTPUTS</span></span>

### <span data-ttu-id="14958-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="14958-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="14958-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14958-131">NOTES</span></span>

## <span data-ttu-id="14958-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14958-132">RELATED LINKS</span></span>
