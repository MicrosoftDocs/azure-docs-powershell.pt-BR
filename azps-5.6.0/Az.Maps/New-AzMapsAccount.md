---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: b6a2e27f18a0ae9b7c98239d5acd1073922e149e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892485"
---
# <span data-ttu-id="40926-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="40926-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="40926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40926-102">SYNOPSIS</span></span>
<span data-ttu-id="40926-103">Cria uma conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="40926-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="40926-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="40926-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40926-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="40926-105">DESCRIPTION</span></span>
<span data-ttu-id="40926-106">O New-AzMapsAccount cmdlet cria uma conta do Azure Maps com a SKU especificada.</span><span class="sxs-lookup"><span data-stu-id="40926-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="40926-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40926-107">EXAMPLES</span></span>

### <span data-ttu-id="40926-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40926-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="40926-109">Cria uma nova conta do Azure Maps chamada MyAccount no grupo de recursos MyResourceGroup com o SKU S0 e uma marca.</span><span class="sxs-lookup"><span data-stu-id="40926-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="40926-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="40926-110">PARAMETERS</span></span>

### <span data-ttu-id="40926-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40926-111">-DefaultProfile</span></span>
<span data-ttu-id="40926-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40926-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40926-113">-Force</span><span class="sxs-lookup"><span data-stu-id="40926-113">-Force</span></span>
<span data-ttu-id="40926-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="40926-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="40926-115">-Name</span><span class="sxs-lookup"><span data-stu-id="40926-115">-Name</span></span>
<span data-ttu-id="40926-116">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="40926-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="40926-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40926-117">-ResourceGroupName</span></span>
<span data-ttu-id="40926-118">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="40926-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="40926-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="40926-119">-SkuName</span></span>
<span data-ttu-id="40926-120">Mapeia o nome Sku da Conta.</span><span class="sxs-lookup"><span data-stu-id="40926-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40926-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="40926-121">-Tag</span></span>
<span data-ttu-id="40926-122">Mapeia marcas de conta.</span><span class="sxs-lookup"><span data-stu-id="40926-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="40926-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40926-123">-Confirm</span></span>
<span data-ttu-id="40926-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40926-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40926-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40926-125">-WhatIf</span></span>
<span data-ttu-id="40926-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40926-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40926-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40926-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40926-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40926-128">CommonParameters</span></span>
<span data-ttu-id="40926-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40926-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40926-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40926-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40926-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40926-131">INPUTS</span></span>

### <span data-ttu-id="40926-132">System.String</span><span class="sxs-lookup"><span data-stu-id="40926-132">System.String</span></span>

## <span data-ttu-id="40926-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="40926-133">OUTPUTS</span></span>

### <span data-ttu-id="40926-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="40926-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="40926-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="40926-135">NOTES</span></span>

## <span data-ttu-id="40926-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40926-136">RELATED LINKS</span></span>
