---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432486"
---
# <span data-ttu-id="b306d-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b306d-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="b306d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b306d-102">SYNOPSIS</span></span>
<span data-ttu-id="b306d-103">Exclui uma conta de serviços com base em localização.</span><span class="sxs-lookup"><span data-stu-id="b306d-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b306d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b306d-104">SYNTAX</span></span>

### <span data-ttu-id="b306d-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b306d-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b306d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b306d-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b306d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b306d-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b306d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b306d-108">DESCRIPTION</span></span>
<span data-ttu-id="b306d-109">O cmdlet **Remove-AzureRmLocationBasedServicesAccount** exclui a conta de serviços com base em local especificada.</span><span class="sxs-lookup"><span data-stu-id="b306d-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="b306d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b306d-110">EXAMPLES</span></span>

### <span data-ttu-id="b306d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b306d-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="b306d-112">Exclui a conta myaccount do grupo de recursos grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b306d-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b306d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b306d-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="b306d-114">Exclui a conta de serviços com base em local especificada.</span><span class="sxs-lookup"><span data-stu-id="b306d-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="b306d-115">OS</span><span class="sxs-lookup"><span data-stu-id="b306d-115">PARAMETERS</span></span>

### <span data-ttu-id="b306d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b306d-116">-DefaultProfile</span></span>
<span data-ttu-id="b306d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b306d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b306d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b306d-118">-InputObject</span></span>
<span data-ttu-id="b306d-119">Conta de serviços baseados em localização canalizada do [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="b306d-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b306d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b306d-120">-Name</span></span>
<span data-ttu-id="b306d-121">Nome da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="b306d-121">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b306d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b306d-122">-ResourceGroupName</span></span>
<span data-ttu-id="b306d-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b306d-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b306d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b306d-124">-ResourceId</span></span>
<span data-ttu-id="b306d-125">Resource Resource da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="b306d-125">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="b306d-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b306d-126">-Confirm</span></span>
<span data-ttu-id="b306d-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b306d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b306d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b306d-128">-WhatIf</span></span>
<span data-ttu-id="b306d-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b306d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b306d-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b306d-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b306d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b306d-131">CommonParameters</span></span>
<span data-ttu-id="b306d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b306d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b306d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b306d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b306d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b306d-134">INPUTS</span></span>

### <span data-ttu-id="b306d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b306d-135">System.String</span></span>

## <span data-ttu-id="b306d-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b306d-136">OUTPUTS</span></span>

### <span data-ttu-id="b306d-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="b306d-137">System.Object</span></span>

## <span data-ttu-id="b306d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b306d-138">NOTES</span></span>

## <span data-ttu-id="b306d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b306d-139">RELATED LINKS</span></span>
