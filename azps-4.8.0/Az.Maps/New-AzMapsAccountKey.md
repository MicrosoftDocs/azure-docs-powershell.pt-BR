---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: c115cd780750770e05bc55b1f70a7cfe33967fff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114455"
---
# <span data-ttu-id="1e4b5-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="1e4b5-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="1e4b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4b5-103">Regenera a chave de uma conta.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-103">Regenerates an account key.</span></span>

## <span data-ttu-id="1e4b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e4b5-104">SYNTAX</span></span>

### <span data-ttu-id="1e4b5-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e4b5-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e4b5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e4b5-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e4b5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e4b5-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e4b5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e4b5-108">DESCRIPTION</span></span>
<span data-ttu-id="1e4b5-109">O cmdlet New-AzMapsAccountKey regenera uma chave de API para uma conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="1e4b5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e4b5-110">EXAMPLES</span></span>

### <span data-ttu-id="1e4b5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1e4b5-111">Example 1</span></span>
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

<span data-ttu-id="1e4b5-112">Regenera a chave de API primária para a conta myaccount no grupo de recursos grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="1e4b5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1e4b5-113">Example 2</span></span>
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

<span data-ttu-id="1e4b5-114">Regenera a chave de API secundária para a conta do Azure Maps especificada.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="1e4b5-115">OS</span><span class="sxs-lookup"><span data-stu-id="1e4b5-115">PARAMETERS</span></span>

### <span data-ttu-id="1e4b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4b5-116">-DefaultProfile</span></span>
<span data-ttu-id="1e4b5-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e4b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e4b5-118">-InputObject</span></span>
<span data-ttu-id="1e4b5-119">Mapeia a conta canalizada do Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="1e4b5-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1e4b5-120">-KeyName</span></span>
<span data-ttu-id="1e4b5-121">Mapeia a chave da conta.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-121">Maps Account Key.</span></span>

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

### <span data-ttu-id="1e4b5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e4b5-122">-Name</span></span>
<span data-ttu-id="1e4b5-123">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="1e4b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e4b5-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1e4b5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e4b5-126">-ResourceId</span></span>
<span data-ttu-id="1e4b5-127">Mapeia ResourceId de conta.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="1e4b5-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e4b5-128">-Confirm</span></span>
<span data-ttu-id="1e4b5-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e4b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e4b5-130">-WhatIf</span></span>
<span data-ttu-id="1e4b5-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e4b5-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e4b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4b5-133">CommonParameters</span></span>
<span data-ttu-id="1e4b5-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4b5-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e4b5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4b5-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e4b5-136">INPUTS</span></span>

### <span data-ttu-id="1e4b5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1e4b5-137">System.String</span></span>

### <span data-ttu-id="1e4b5-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1e4b5-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="1e4b5-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e4b5-139">OUTPUTS</span></span>

### <span data-ttu-id="1e4b5-140">Microsoft. Azure. Management. Maps. Models. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1e4b5-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="1e4b5-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e4b5-141">NOTES</span></span>

## <span data-ttu-id="1e4b5-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e4b5-142">RELATED LINKS</span></span>
