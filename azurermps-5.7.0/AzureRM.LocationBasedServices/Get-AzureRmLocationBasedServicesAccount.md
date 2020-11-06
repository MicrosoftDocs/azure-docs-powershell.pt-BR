---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428894"
---
# <span data-ttu-id="ae5d5-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ae5d5-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="ae5d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5d5-103">Obtém a conta.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae5d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae5d5-104">SYNTAX</span></span>

### <span data-ttu-id="ae5d5-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae5d5-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae5d5-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae5d5-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae5d5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae5d5-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae5d5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae5d5-108">DESCRIPTION</span></span>
<span data-ttu-id="ae5d5-109">O cmdlet **Get-AzureRmLocationBasedServicesAccount** Obtém uma conta de serviços com base em um local provisionado, seja por grupo de recursos e nome ou por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="ae5d5-110">Além disso, ele pode retornar uma lista de todas as contas no nome da fonte ou de todas as contas de serviços com base em locais para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="ae5d5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae5d5-111">EXAMPLES</span></span>

### <span data-ttu-id="ae5d5-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae5d5-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="ae5d5-113">Obtém a conta chamada myaccount no grupo de recursos MyResource, se existir.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="ae5d5-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ae5d5-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="ae5d5-115">Obtém todas as contas de serviços com base no local no grupo MyResource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="ae5d5-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ae5d5-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="ae5d5-117">Obtém todas as contas de serviços baseadas em local na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="ae5d5-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ae5d5-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="ae5d5-119">Obtém a conta de serviços com base no local especificada pela ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="ae5d5-120">OS</span><span class="sxs-lookup"><span data-stu-id="ae5d5-120">PARAMETERS</span></span>

### <span data-ttu-id="ae5d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5d5-121">-DefaultProfile</span></span>
<span data-ttu-id="ae5d5-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5d5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae5d5-123">-Name</span></span>
<span data-ttu-id="ae5d5-124">Nome da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae5d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae5d5-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5d5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae5d5-127">-ResourceId</span></span>
<span data-ttu-id="ae5d5-128">Resource Resource da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5d5-129">CommonParameters</span></span>
<span data-ttu-id="ae5d5-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5d5-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5d5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5d5-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae5d5-132">INPUTS</span></span>

### <span data-ttu-id="ae5d5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ae5d5-133">System.String</span></span>

## <span data-ttu-id="ae5d5-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae5d5-134">OUTPUTS</span></span>

### <span data-ttu-id="ae5d5-135">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ae5d5-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="ae5d5-136">Esse cmdlet retorna um objeto **PSLocationBasedServicesAccount** .</span><span class="sxs-lookup"><span data-stu-id="ae5d5-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="ae5d5-137">Você pode modificar esse objeto e, em seguida, aplicar as alterações usando **set-AzureRmLocationBasedServices**.</span><span class="sxs-lookup"><span data-stu-id="ae5d5-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="ae5d5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae5d5-138">NOTES</span></span>

## <span data-ttu-id="ae5d5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae5d5-139">RELATED LINKS</span></span>
