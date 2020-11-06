---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
ms.openlocfilehash: 13364cde6799a6d99bcdba1d5cd2078c3392a2cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430875"
---
# <span data-ttu-id="d9ab7-101">New-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="d9ab7-101">New-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="d9ab7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ab7-103">Regenera a chave de uma conta.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9ab7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9ab7-104">SYNTAX</span></span>

### <span data-ttu-id="d9ab7-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9ab7-105">NameParameterSet (Default)</span></span>
```
New-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ab7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9ab7-106">InputObjectParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ab7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9ab7-107">ResourceIdParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ab7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9ab7-108">DESCRIPTION</span></span>
<span data-ttu-id="d9ab7-109">O cmdlet New-AzureRmMapsAccountKey regenera uma chave de API para uma conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-109">The New-AzureRmMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="d9ab7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9ab7-110">EXAMPLES</span></span>

### <span data-ttu-id="d9ab7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d9ab7-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="d9ab7-112">Regenera a chave de API primária para a conta myaccount no grupo de recursos grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="d9ab7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d9ab7-113">Example 2</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="d9ab7-114">Regenera a chave de API secundária para a conta do Azure Maps especificada.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="d9ab7-115">OS</span><span class="sxs-lookup"><span data-stu-id="d9ab7-115">PARAMETERS</span></span>

### <span data-ttu-id="d9ab7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ab7-116">-DefaultProfile</span></span>
<span data-ttu-id="d9ab7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9ab7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9ab7-118">-InputObject</span></span>
<span data-ttu-id="d9ab7-119">Mapeia a conta canalizada do Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ab7-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d9ab7-120">-KeyName</span></span>
<span data-ttu-id="d9ab7-121">Mapeia a chave da conta.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ab7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9ab7-122">-Name</span></span>
<span data-ttu-id="d9ab7-123">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ab7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ab7-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9ab7-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ab7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9ab7-126">-ResourceId</span></span>
<span data-ttu-id="d9ab7-127">Mapeia ResourceId de conta.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="d9ab7-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9ab7-128">-Confirm</span></span>
<span data-ttu-id="d9ab7-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ab7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ab7-130">-WhatIf</span></span>
<span data-ttu-id="d9ab7-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ab7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ab7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ab7-133">CommonParameters</span></span>
<span data-ttu-id="d9ab7-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ab7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ab7-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ab7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ab7-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9ab7-136">INPUTS</span></span>

### <span data-ttu-id="d9ab7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d9ab7-137">System.String</span></span>

### <span data-ttu-id="d9ab7-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="d9ab7-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="d9ab7-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9ab7-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d9ab7-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9ab7-140">OUTPUTS</span></span>

### <span data-ttu-id="d9ab7-141">Microsoft. Azure. Management. Maps. Models. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d9ab7-141">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="d9ab7-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9ab7-142">NOTES</span></span>

## <span data-ttu-id="d9ab7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9ab7-143">RELATED LINKS</span></span>
