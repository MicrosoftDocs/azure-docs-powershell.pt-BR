---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: 420cf84bb946df3d7f2110937aa332e25978aa8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890837"
---
# <span data-ttu-id="9fad9-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="9fad9-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="9fad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fad9-102">SYNOPSIS</span></span>
<span data-ttu-id="9fad9-103">Obtém a conta.</span><span class="sxs-lookup"><span data-stu-id="9fad9-103">Gets the account.</span></span>

## <span data-ttu-id="9fad9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9fad9-104">SYNTAX</span></span>

### <span data-ttu-id="9fad9-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9fad9-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fad9-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fad9-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fad9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fad9-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fad9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9fad9-108">DESCRIPTION</span></span>
<span data-ttu-id="9fad9-109">O Get-AzMapsAccount cmdlet obtém uma conta provisionada do Azure Maps, por grupo de recursos e nome, ou por ID de recurso. Além disso, ele pode retornar uma lista de todas as contas no ResourceGroup ou todas as contas do Azure Maps para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9fad9-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="9fad9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fad9-110">EXAMPLES</span></span>

### <span data-ttu-id="9fad9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9fad9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="9fad9-112">Obtém a conta chamada MyAccount no grupo de recursos MyResourceGroup, se ela existir.</span><span class="sxs-lookup"><span data-stu-id="9fad9-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="9fad9-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9fad9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="9fad9-114">Obtém todas as contas do Azure Maps no grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9fad9-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="9fad9-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9fad9-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="9fad9-116">Obtém todas as contas do Azure Maps na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9fad9-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="9fad9-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="9fad9-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="9fad9-118">Obtém a conta Mapas especificada pela ID de Recurso.</span><span class="sxs-lookup"><span data-stu-id="9fad9-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="9fad9-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9fad9-119">PARAMETERS</span></span>

### <span data-ttu-id="9fad9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fad9-120">-DefaultProfile</span></span>
<span data-ttu-id="9fad9-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fad9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fad9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9fad9-122">-Name</span></span>
<span data-ttu-id="9fad9-123">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="9fad9-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fad9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fad9-124">-ResourceGroupName</span></span>
<span data-ttu-id="9fad9-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="9fad9-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fad9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fad9-126">-ResourceId</span></span>
<span data-ttu-id="9fad9-127">Mapeia ResourceId da conta.</span><span class="sxs-lookup"><span data-stu-id="9fad9-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fad9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fad9-128">CommonParameters</span></span>
<span data-ttu-id="9fad9-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fad9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fad9-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fad9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fad9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fad9-131">INPUTS</span></span>

### <span data-ttu-id="9fad9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9fad9-132">System.String</span></span>

## <span data-ttu-id="9fad9-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9fad9-133">OUTPUTS</span></span>

### <span data-ttu-id="9fad9-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="9fad9-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="9fad9-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="9fad9-135">NOTES</span></span>

## <span data-ttu-id="9fad9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fad9-136">RELATED LINKS</span></span>
