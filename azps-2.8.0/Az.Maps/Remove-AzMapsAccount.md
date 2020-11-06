---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: ba474ca3ea3a975262eec8b98df1fb99b0f336cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595914"
---
# <span data-ttu-id="e3578-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e3578-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="e3578-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3578-102">SYNOPSIS</span></span>
<span data-ttu-id="e3578-103">Exclui uma conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="e3578-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="e3578-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3578-104">SYNTAX</span></span>

### <span data-ttu-id="e3578-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e3578-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3578-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3578-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3578-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3578-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3578-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3578-108">DESCRIPTION</span></span>
<span data-ttu-id="e3578-109">O cmdlet Remove-AzMapsAccount exclui a conta do Azure Maps especificada.</span><span class="sxs-lookup"><span data-stu-id="e3578-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="e3578-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3578-110">EXAMPLES</span></span>

### <span data-ttu-id="e3578-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3578-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e3578-112">Exclui a conta myaccount do grupo de recursos grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3578-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e3578-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e3578-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e3578-114">Exclui a conta do Azure Maps especificada.</span><span class="sxs-lookup"><span data-stu-id="e3578-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="e3578-115">OS</span><span class="sxs-lookup"><span data-stu-id="e3578-115">PARAMETERS</span></span>

### <span data-ttu-id="e3578-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3578-116">-DefaultProfile</span></span>
<span data-ttu-id="e3578-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3578-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3578-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3578-118">-InputObject</span></span>
<span data-ttu-id="e3578-119">Mapeia a conta canalizada do Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="e3578-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="e3578-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3578-120">-Name</span></span>
<span data-ttu-id="e3578-121">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="e3578-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="e3578-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3578-122">-PassThru</span></span>
<span data-ttu-id="e3578-123">Retorne se a conta especificada foi excluída ou não com êxito.</span><span class="sxs-lookup"><span data-stu-id="e3578-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="e3578-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3578-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3578-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3578-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="e3578-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3578-126">-ResourceId</span></span>
<span data-ttu-id="e3578-127">Mapeia ResourceId de conta.</span><span class="sxs-lookup"><span data-stu-id="e3578-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="e3578-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e3578-128">-Confirm</span></span>
<span data-ttu-id="e3578-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3578-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3578-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3578-130">-WhatIf</span></span>
<span data-ttu-id="e3578-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3578-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3578-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3578-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3578-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3578-133">CommonParameters</span></span>
<span data-ttu-id="e3578-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3578-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3578-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3578-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3578-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3578-136">INPUTS</span></span>

### <span data-ttu-id="e3578-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e3578-137">System.String</span></span>

### <span data-ttu-id="e3578-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e3578-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="e3578-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3578-139">OUTPUTS</span></span>

### <span data-ttu-id="e3578-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3578-140">System.Boolean</span></span>

## <span data-ttu-id="e3578-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3578-141">NOTES</span></span>

## <span data-ttu-id="e3578-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3578-142">RELATED LINKS</span></span>
