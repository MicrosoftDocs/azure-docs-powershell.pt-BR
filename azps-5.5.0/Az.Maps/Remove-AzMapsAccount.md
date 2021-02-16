---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118433"
---
# <span data-ttu-id="67da2-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="67da2-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="67da2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67da2-102">SYNOPSIS</span></span>
<span data-ttu-id="67da2-103">Exclui uma conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="67da2-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="67da2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67da2-104">SYNTAX</span></span>

### <span data-ttu-id="67da2-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="67da2-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67da2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67da2-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67da2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67da2-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67da2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="67da2-108">DESCRIPTION</span></span>
<span data-ttu-id="67da2-109">O Remove-AzMapsAccount cmdlet exclui a conta especificada do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="67da2-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="67da2-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="67da2-110">EXAMPLES</span></span>

### <span data-ttu-id="67da2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67da2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="67da2-112">Exclui a conta MyAccount do grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="67da2-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="67da2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="67da2-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="67da2-114">Exclui a Conta de Mapas do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="67da2-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="67da2-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67da2-115">PARAMETERS</span></span>

### <span data-ttu-id="67da2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67da2-116">-DefaultProfile</span></span>
<span data-ttu-id="67da2-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67da2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67da2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67da2-118">-InputObject</span></span>
<span data-ttu-id="67da2-119">Conta de Mapas canalada de Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="67da2-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="67da2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="67da2-120">-Name</span></span>
<span data-ttu-id="67da2-121">Nome da Conta do Mapas.</span><span class="sxs-lookup"><span data-stu-id="67da2-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="67da2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67da2-122">-PassThru</span></span>
<span data-ttu-id="67da2-123">Retorne se a conta especificada foi excluída com êxito ou não.</span><span class="sxs-lookup"><span data-stu-id="67da2-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="67da2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67da2-124">-ResourceGroupName</span></span>
<span data-ttu-id="67da2-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="67da2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="67da2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67da2-126">-ResourceId</span></span>
<span data-ttu-id="67da2-127">Mapeia o ResourceId da Conta.</span><span class="sxs-lookup"><span data-stu-id="67da2-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="67da2-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="67da2-128">-Confirm</span></span>
<span data-ttu-id="67da2-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67da2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67da2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67da2-130">-WhatIf</span></span>
<span data-ttu-id="67da2-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="67da2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67da2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67da2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67da2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67da2-133">CommonParameters</span></span>
<span data-ttu-id="67da2-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67da2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67da2-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67da2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67da2-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="67da2-136">INPUTS</span></span>

### <span data-ttu-id="67da2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="67da2-137">System.String</span></span>

### <span data-ttu-id="67da2-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="67da2-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="67da2-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="67da2-139">OUTPUTS</span></span>

### <span data-ttu-id="67da2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67da2-140">System.Boolean</span></span>

## <span data-ttu-id="67da2-141">Notas</span><span class="sxs-lookup"><span data-stu-id="67da2-141">NOTES</span></span>

## <span data-ttu-id="67da2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67da2-142">RELATED LINKS</span></span>
