---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 7116cd4c5da2dd897af4e6540593a5e5458e4eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429760"
---
# <span data-ttu-id="fcea6-101">New-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="fcea6-101">New-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="fcea6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcea6-102">SYNOPSIS</span></span>
<span data-ttu-id="fcea6-103">Regenera a chave de uma conta.</span><span class="sxs-lookup"><span data-stu-id="fcea6-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcea6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcea6-104">SYNTAX</span></span>

### <span data-ttu-id="fcea6-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fcea6-105">NameParameterSet (Default)</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcea6-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcea6-106">InputObjectParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcea6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcea6-107">ResourceIdParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcea6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcea6-108">DESCRIPTION</span></span>
<span data-ttu-id="fcea6-109">O cmdlet **New-AzureRmLocationBasedServicesAccountKey** regenera uma chave de API para uma conta de serviços com base em local.</span><span class="sxs-lookup"><span data-stu-id="fcea6-109">The **New-AzureRmLocationBasedServicesAccountKey** cmdlet regenerates an API key for a Location Based Services account.</span></span>

## <span data-ttu-id="fcea6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcea6-110">EXAMPLES</span></span>

### <span data-ttu-id="fcea6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fcea6-111">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="fcea6-112">Regenera a chave de API primária para a conta myaccount no grupo de recursos grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcea6-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="fcea6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fcea6-113">Example 2</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="fcea6-114">Regenera a chave de API secundária para a conta de serviços com base em local especificada.</span><span class="sxs-lookup"><span data-stu-id="fcea6-114">Regenerates the Secondary API Key for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="fcea6-115">OS</span><span class="sxs-lookup"><span data-stu-id="fcea6-115">PARAMETERS</span></span>

### <span data-ttu-id="fcea6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcea6-116">-DefaultProfile</span></span>
<span data-ttu-id="fcea6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcea6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcea6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcea6-118">-InputObject</span></span>
<span data-ttu-id="fcea6-119">Conta de serviços baseados em localização canalizada do [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="fcea6-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

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

### <span data-ttu-id="fcea6-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fcea6-120">-KeyName</span></span>
<span data-ttu-id="fcea6-121">Chave da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="fcea6-121">Location Based Services Account Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcea6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcea6-122">-Name</span></span>
<span data-ttu-id="fcea6-123">Nome da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="fcea6-123">Location Based Services Account Name.</span></span>

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

### <span data-ttu-id="fcea6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcea6-124">-ResourceGroupName</span></span>
<span data-ttu-id="fcea6-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcea6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcea6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcea6-126">-ResourceId</span></span>
<span data-ttu-id="fcea6-127">Resource Resource da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="fcea6-127">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="fcea6-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fcea6-128">-Confirm</span></span>
<span data-ttu-id="fcea6-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcea6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcea6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcea6-130">-WhatIf</span></span>
<span data-ttu-id="fcea6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fcea6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcea6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcea6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcea6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcea6-133">CommonParameters</span></span>
<span data-ttu-id="fcea6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcea6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcea6-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcea6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcea6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcea6-136">INPUTS</span></span>

### <span data-ttu-id="fcea6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fcea6-137">System.String</span></span>
<span data-ttu-id="fcea6-138">Microsoft. Azure. Commands. LocationBasedServices. NewAzureLocationBasedServicesAccountKeyCommand + keynametype</span><span class="sxs-lookup"><span data-stu-id="fcea6-138">Microsoft.Azure.Commands.LocationBasedServices.NewAzureLocationBasedServicesAccountKeyCommand+KeyNameType</span></span>

## <span data-ttu-id="fcea6-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcea6-139">OUTPUTS</span></span>

### <span data-ttu-id="fcea6-140">Microsoft. Azure. Management. LocationBasedServices. Models. LocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fcea6-140">Microsoft.Azure.Management.LocationBasedServices.Models.LocationBasedServicesAccountKeys</span></span>

## <span data-ttu-id="fcea6-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcea6-141">NOTES</span></span>

## <span data-ttu-id="fcea6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcea6-142">RELATED LINKS</span></span>
