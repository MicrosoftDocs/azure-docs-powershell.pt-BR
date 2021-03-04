---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: 6c0843afa3001299a21f49cec5ed73f74bdcd2a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885863"
---
# <span data-ttu-id="dbac7-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="dbac7-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="dbac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbac7-102">SYNOPSIS</span></span>
<span data-ttu-id="dbac7-103">Cria um novo ou atualiza um grupo de ações existente.</span><span class="sxs-lookup"><span data-stu-id="dbac7-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="dbac7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dbac7-104">SYNTAX</span></span>

### <span data-ttu-id="dbac7-105">ByPropertyName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dbac7-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbac7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dbac7-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbac7-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dbac7-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbac7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dbac7-108">DESCRIPTION</span></span>
<span data-ttu-id="dbac7-109">O cmdlet **Set-AzActionGroup** cria um novo ou atualiza um grupo de ações existente</span><span class="sxs-lookup"><span data-stu-id="dbac7-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="dbac7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbac7-110">EXAMPLES</span></span>

### <span data-ttu-id="dbac7-111">Exemplo 1: Criar um Grupo de Ações</span><span class="sxs-lookup"><span data-stu-id="dbac7-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="dbac7-112">Os dois primeiros comandos criam dois receptores.</span><span class="sxs-lookup"><span data-stu-id="dbac7-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="dbac7-113">O comando final cria um Grupo de Ações, incluindo os dois receptores.</span><span class="sxs-lookup"><span data-stu-id="dbac7-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="dbac7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dbac7-114">PARAMETERS</span></span>

### <span data-ttu-id="dbac7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbac7-115">-DefaultProfile</span></span>
<span data-ttu-id="dbac7-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="dbac7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbac7-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="dbac7-117">-DisableGroup</span></span>
<span data-ttu-id="dbac7-118">Desabilita o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="dbac7-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbac7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbac7-119">-InputObject</span></span>
<span data-ttu-id="dbac7-120">O recurso do grupo de ações</span><span class="sxs-lookup"><span data-stu-id="dbac7-120">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbac7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dbac7-121">-Name</span></span>
<span data-ttu-id="dbac7-122">O nome do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="dbac7-122">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbac7-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="dbac7-123">-Receiver</span></span>
<span data-ttu-id="dbac7-124">A lista de receptores do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="dbac7-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbac7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbac7-125">-ResourceGroupName</span></span>
<span data-ttu-id="dbac7-126">O nam do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dbac7-126">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbac7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbac7-127">-ResourceId</span></span>
<span data-ttu-id="dbac7-128">O recurso i</span><span class="sxs-lookup"><span data-stu-id="dbac7-128">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbac7-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="dbac7-129">-ShortName</span></span>
<span data-ttu-id="dbac7-130">O nome curto do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="dbac7-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbac7-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="dbac7-131">-Tag</span></span>
<span data-ttu-id="dbac7-132">As marcas do recurso do grupo de ações</span><span class="sxs-lookup"><span data-stu-id="dbac7-132">The tags of the action group resource</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbac7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbac7-133">-Confirm</span></span>
<span data-ttu-id="dbac7-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbac7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbac7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbac7-135">-WhatIf</span></span>
<span data-ttu-id="dbac7-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dbac7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbac7-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dbac7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbac7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbac7-138">CommonParameters</span></span>
<span data-ttu-id="dbac7-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbac7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbac7-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbac7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbac7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbac7-141">INPUTS</span></span>

### <span data-ttu-id="dbac7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dbac7-142">System.String</span></span>

### <span data-ttu-id="dbac7-143">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="dbac7-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dbac7-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dbac7-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dbac7-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dbac7-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dbac7-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="dbac7-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="dbac7-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dbac7-147">OUTPUTS</span></span>

### <span data-ttu-id="dbac7-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="dbac7-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="dbac7-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="dbac7-149">NOTES</span></span>

## <span data-ttu-id="dbac7-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbac7-150">RELATED LINKS</span></span>

<span data-ttu-id="dbac7-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="dbac7-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
