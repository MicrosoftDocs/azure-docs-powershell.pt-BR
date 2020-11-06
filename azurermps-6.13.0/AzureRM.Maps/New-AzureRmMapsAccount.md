---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
ms.openlocfilehash: 0b8bfad1b3bb9f24c6b7c74e92f64c64d776c2d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430877"
---
# <span data-ttu-id="5df31-101">New-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="5df31-101">New-AzureRmMapsAccount</span></span>

## <span data-ttu-id="5df31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5df31-102">SYNOPSIS</span></span>
<span data-ttu-id="5df31-103">Cria uma conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="5df31-103">Creates an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5df31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5df31-104">SYNTAX</span></span>

```
New-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df31-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5df31-105">DESCRIPTION</span></span>
<span data-ttu-id="5df31-106">O cmdlet New-AzureRmMapsAccount cria uma conta do Azure Maps com a SKU especificada.</span><span class="sxs-lookup"><span data-stu-id="5df31-106">The New-AzureRmMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="5df31-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5df31-107">EXAMPLES</span></span>

### <span data-ttu-id="5df31-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5df31-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="5df31-109">Cria uma nova conta do Azure Maps chamada myaccount no grupo de recursos grupo de recursos com o SKU S0 e uma marca.</span><span class="sxs-lookup"><span data-stu-id="5df31-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="5df31-110">OS</span><span class="sxs-lookup"><span data-stu-id="5df31-110">PARAMETERS</span></span>

### <span data-ttu-id="5df31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df31-111">-DefaultProfile</span></span>
<span data-ttu-id="5df31-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5df31-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df31-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5df31-113">-Force</span></span>
<span data-ttu-id="5df31-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5df31-114">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df31-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5df31-115">-Name</span></span>
<span data-ttu-id="5df31-116">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="5df31-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df31-117">-ResourceGroupName</span></span>
<span data-ttu-id="5df31-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5df31-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df31-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5df31-119">-SkuName</span></span>
<span data-ttu-id="5df31-120">Mapeia o nome SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="5df31-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df31-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="5df31-121">-Tag</span></span>
<span data-ttu-id="5df31-122">Mapeia marcas de conta.</span><span class="sxs-lookup"><span data-stu-id="5df31-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df31-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5df31-123">-Confirm</span></span>
<span data-ttu-id="5df31-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5df31-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df31-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df31-125">-WhatIf</span></span>
<span data-ttu-id="5df31-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5df31-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df31-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5df31-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df31-128">CommonParameters</span></span>
<span data-ttu-id="5df31-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df31-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df31-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df31-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5df31-131">INPUTS</span></span>

### <span data-ttu-id="5df31-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5df31-132">System.String</span></span>

## <span data-ttu-id="5df31-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5df31-133">OUTPUTS</span></span>

### <span data-ttu-id="5df31-134">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="5df31-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="5df31-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5df31-135">NOTES</span></span>

## <span data-ttu-id="5df31-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5df31-136">RELATED LINKS</span></span>
