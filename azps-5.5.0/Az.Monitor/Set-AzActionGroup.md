---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: b10aad8cdf480dd567b0646fb3befa95fb32bf72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114760"
---
# <span data-ttu-id="f3dbf-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="f3dbf-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="f3dbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="f3dbf-103">Cria um novo ou atualiza um grupo de ações existente.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="f3dbf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3dbf-104">SYNTAX</span></span>

### <span data-ttu-id="f3dbf-105">ByPropertyName (Default)</span><span class="sxs-lookup"><span data-stu-id="f3dbf-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3dbf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3dbf-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3dbf-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f3dbf-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3dbf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3dbf-108">DESCRIPTION</span></span>
<span data-ttu-id="f3dbf-109">O **cmdlet Set-AzActionGroup** cria um novo ou atualiza um grupo de ações existente</span><span class="sxs-lookup"><span data-stu-id="f3dbf-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="f3dbf-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3dbf-110">EXAMPLES</span></span>

### <span data-ttu-id="f3dbf-111">Exemplo 1: Criar um Grupo de Ações</span><span class="sxs-lookup"><span data-stu-id="f3dbf-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="f3dbf-112">Os dois primeiros comandos criam dois receptores.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="f3dbf-113">O comando final cria um Grupo de Ações, incluindo os dois receptores.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="f3dbf-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3dbf-114">PARAMETERS</span></span>

### <span data-ttu-id="f3dbf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3dbf-115">-DefaultProfile</span></span>
<span data-ttu-id="f3dbf-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f3dbf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3dbf-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="f3dbf-117">-DisableGroup</span></span>
<span data-ttu-id="f3dbf-118">Desabilita o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-118">Disables the action group.</span></span>

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

### <span data-ttu-id="f3dbf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3dbf-119">-InputObject</span></span>
<span data-ttu-id="f3dbf-120">O recurso de grupo de ações</span><span class="sxs-lookup"><span data-stu-id="f3dbf-120">The action group resource</span></span>

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

### <span data-ttu-id="f3dbf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3dbf-121">-Name</span></span>
<span data-ttu-id="f3dbf-122">O nome do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-122">The name of the action group.</span></span>

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

### <span data-ttu-id="f3dbf-123">-Receptor</span><span class="sxs-lookup"><span data-stu-id="f3dbf-123">-Receiver</span></span>
<span data-ttu-id="f3dbf-124">A lista de receptores do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="f3dbf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3dbf-125">-ResourceGroupName</span></span>
<span data-ttu-id="f3dbf-126">A nam do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f3dbf-126">The resource group nam</span></span>

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

### <span data-ttu-id="f3dbf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3dbf-127">-ResourceId</span></span>
<span data-ttu-id="f3dbf-128">O recurso i</span><span class="sxs-lookup"><span data-stu-id="f3dbf-128">The resource i</span></span>

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

### <span data-ttu-id="f3dbf-129">-Nome Curto</span><span class="sxs-lookup"><span data-stu-id="f3dbf-129">-ShortName</span></span>
<span data-ttu-id="f3dbf-130">O nome curto do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="f3dbf-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3dbf-131">-Tag</span></span>
<span data-ttu-id="f3dbf-132">As marcas do recurso de grupo de ações</span><span class="sxs-lookup"><span data-stu-id="f3dbf-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="f3dbf-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f3dbf-133">-Confirm</span></span>
<span data-ttu-id="f3dbf-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3dbf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3dbf-135">-WhatIf</span></span>
<span data-ttu-id="f3dbf-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3dbf-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3dbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3dbf-138">CommonParameters</span></span>
<span data-ttu-id="f3dbf-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3dbf-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3dbf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3dbf-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="f3dbf-141">INPUTS</span></span>

### <span data-ttu-id="f3dbf-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f3dbf-142">System.String</span></span>

### <span data-ttu-id="f3dbf-143">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f3dbf-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f3dbf-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f3dbf-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f3dbf-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f3dbf-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f3dbf-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="f3dbf-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="f3dbf-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="f3dbf-147">OUTPUTS</span></span>

### <span data-ttu-id="f3dbf-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="f3dbf-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="f3dbf-149">Notas</span><span class="sxs-lookup"><span data-stu-id="f3dbf-149">NOTES</span></span>

## <span data-ttu-id="f3dbf-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3dbf-150">RELATED LINKS</span></span>

<span data-ttu-id="f3dbf-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="f3dbf-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
