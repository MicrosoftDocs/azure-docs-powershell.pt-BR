---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
ms.openlocfilehash: 68ccff91f6e233862ba1ee5aa94a3a3d0d8422b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440373"
---
# <span data-ttu-id="a02db-101">Get-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="a02db-101">Get-AzureRmMapsAccount</span></span>

## <span data-ttu-id="a02db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a02db-102">SYNOPSIS</span></span>
<span data-ttu-id="a02db-103">Obtém a conta.</span><span class="sxs-lookup"><span data-stu-id="a02db-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a02db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a02db-104">SYNTAX</span></span>

### <span data-ttu-id="a02db-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a02db-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a02db-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a02db-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a02db-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a02db-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a02db-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a02db-108">DESCRIPTION</span></span>
<span data-ttu-id="a02db-109">O cmdlet Get-AzureRmMapsAccount Obtém uma conta provisionada do Azure Maps, seja por grupo de recursos e nome ou por ID do recurso. Além disso, ele pode retornar uma lista de todas as contas no MySource ou todas as contas do Azure Maps para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a02db-109">The Get-AzureRmMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="a02db-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a02db-110">EXAMPLES</span></span>

### <span data-ttu-id="a02db-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a02db-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="a02db-112">Obtém a conta chamada myaccount no grupo de recursos MyResource, se existir.</span><span class="sxs-lookup"><span data-stu-id="a02db-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="a02db-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a02db-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="a02db-114">Obtém todas as contas do Azure Maps no grupo MyResource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a02db-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="a02db-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a02db-115">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="a02db-116">Obtém todas as contas do Azure Maps na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a02db-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="a02db-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="a02db-117">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="a02db-118">Obtém a conta de mapas especificada pela ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a02db-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="a02db-119">OS</span><span class="sxs-lookup"><span data-stu-id="a02db-119">PARAMETERS</span></span>

### <span data-ttu-id="a02db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02db-120">-DefaultProfile</span></span>
<span data-ttu-id="a02db-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a02db-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02db-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a02db-122">-Name</span></span>
<span data-ttu-id="a02db-123">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="a02db-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="a02db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a02db-124">-ResourceGroupName</span></span>
<span data-ttu-id="a02db-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a02db-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a02db-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a02db-126">-ResourceId</span></span>
<span data-ttu-id="a02db-127">Mapeia ResourceId de conta.</span><span class="sxs-lookup"><span data-stu-id="a02db-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="a02db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02db-128">CommonParameters</span></span>
<span data-ttu-id="a02db-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a02db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02db-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a02db-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02db-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a02db-131">INPUTS</span></span>

### <span data-ttu-id="a02db-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a02db-132">System.String</span></span>

## <span data-ttu-id="a02db-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a02db-133">OUTPUTS</span></span>

### <span data-ttu-id="a02db-134">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="a02db-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="a02db-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a02db-135">NOTES</span></span>

## <span data-ttu-id="a02db-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a02db-136">RELATED LINKS</span></span>
