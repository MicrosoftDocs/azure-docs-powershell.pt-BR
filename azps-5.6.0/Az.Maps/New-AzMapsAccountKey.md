---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: 4892e5e31c67725d15af7be015ca27bd450babd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892483"
---
# <span data-ttu-id="b44ef-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="b44ef-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="b44ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b44ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b44ef-103">Regenera uma chave de conta.</span><span class="sxs-lookup"><span data-stu-id="b44ef-103">Regenerates an account key.</span></span>

## <span data-ttu-id="b44ef-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b44ef-104">SYNTAX</span></span>

### <span data-ttu-id="b44ef-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b44ef-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b44ef-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b44ef-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b44ef-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b44ef-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b44ef-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b44ef-108">DESCRIPTION</span></span>
<span data-ttu-id="b44ef-109">O New-AzMapsAccountKey cmdlet regenera uma chave de API para uma conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="b44ef-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="b44ef-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b44ef-110">EXAMPLES</span></span>

### <span data-ttu-id="b44ef-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b44ef-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="b44ef-112">Regenera a Chave principal da API da conta MyAccount no grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b44ef-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b44ef-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b44ef-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="b44ef-114">Regenera a Chave de API Secundária para a Conta de Mapas do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="b44ef-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="b44ef-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b44ef-115">PARAMETERS</span></span>

### <span data-ttu-id="b44ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44ef-116">-DefaultProfile</span></span>
<span data-ttu-id="b44ef-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b44ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b44ef-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b44ef-118">-InputObject</span></span>
<span data-ttu-id="b44ef-119">Mapas Conta canalização de Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="b44ef-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="b44ef-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b44ef-120">-KeyName</span></span>
<span data-ttu-id="b44ef-121">Mapeia a Chave da Conta.</span><span class="sxs-lookup"><span data-stu-id="b44ef-121">Maps Account Key.</span></span>

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

### <span data-ttu-id="b44ef-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b44ef-122">-Name</span></span>
<span data-ttu-id="b44ef-123">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="b44ef-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="b44ef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b44ef-124">-ResourceGroupName</span></span>
<span data-ttu-id="b44ef-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="b44ef-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b44ef-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b44ef-126">-ResourceId</span></span>
<span data-ttu-id="b44ef-127">Mapeia ResourceId da conta.</span><span class="sxs-lookup"><span data-stu-id="b44ef-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="b44ef-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b44ef-128">-Confirm</span></span>
<span data-ttu-id="b44ef-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b44ef-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b44ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b44ef-130">-WhatIf</span></span>
<span data-ttu-id="b44ef-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b44ef-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b44ef-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b44ef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b44ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44ef-133">CommonParameters</span></span>
<span data-ttu-id="b44ef-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b44ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44ef-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b44ef-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44ef-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b44ef-136">INPUTS</span></span>

### <span data-ttu-id="b44ef-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b44ef-137">System.String</span></span>

### <span data-ttu-id="b44ef-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b44ef-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="b44ef-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b44ef-139">OUTPUTS</span></span>

### <span data-ttu-id="b44ef-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b44ef-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="b44ef-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="b44ef-141">NOTES</span></span>

## <span data-ttu-id="b44ef-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b44ef-142">RELATED LINKS</span></span>
