---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: 40e9e6978b71f781644f1ceb853403b3b805f448
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600790"
---
# <span data-ttu-id="dea3f-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="dea3f-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="dea3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dea3f-102">SYNOPSIS</span></span>
<span data-ttu-id="dea3f-103">Cria uma nova ou atualiza um grupo de ações existente.</span><span class="sxs-lookup"><span data-stu-id="dea3f-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="dea3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dea3f-104">SYNTAX</span></span>

### <span data-ttu-id="dea3f-105">ByPropertyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="dea3f-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dea3f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dea3f-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dea3f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dea3f-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dea3f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dea3f-108">DESCRIPTION</span></span>
<span data-ttu-id="dea3f-109">O cmdlet **set-AzActionGroup** cria um novo ou atualiza um grupo de ações existente</span><span class="sxs-lookup"><span data-stu-id="dea3f-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="dea3f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dea3f-110">EXAMPLES</span></span>

### <span data-ttu-id="dea3f-111">Exemplo 1: criar um grupo de ação</span><span class="sxs-lookup"><span data-stu-id="dea3f-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="dea3f-112">Os dois primeiros comandos criam dois destinatários.</span><span class="sxs-lookup"><span data-stu-id="dea3f-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="dea3f-113">O comando final cria um grupo de ação incluindo os dois destinatários.</span><span class="sxs-lookup"><span data-stu-id="dea3f-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="dea3f-114">OS</span><span class="sxs-lookup"><span data-stu-id="dea3f-114">PARAMETERS</span></span>

### <span data-ttu-id="dea3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea3f-115">-DefaultProfile</span></span>
<span data-ttu-id="dea3f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dea3f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dea3f-117">-Desativar o</span><span class="sxs-lookup"><span data-stu-id="dea3f-117">-DisableGroup</span></span>
<span data-ttu-id="dea3f-118">Desabilita o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="dea3f-118">Disables the action group.</span></span>

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

### <span data-ttu-id="dea3f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dea3f-119">-InputObject</span></span>
<span data-ttu-id="dea3f-120">O grupo de ação resourc</span><span class="sxs-lookup"><span data-stu-id="dea3f-120">The action group resourc</span></span>

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

### <span data-ttu-id="dea3f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="dea3f-121">-Name</span></span>
<span data-ttu-id="dea3f-122">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="dea3f-122">The name of the action group.</span></span>

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

### <span data-ttu-id="dea3f-123">-Receptor</span><span class="sxs-lookup"><span data-stu-id="dea3f-123">-Receiver</span></span>
<span data-ttu-id="dea3f-124">A lista de destinatários do grupo ação.</span><span class="sxs-lookup"><span data-stu-id="dea3f-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="dea3f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dea3f-125">-ResourceGroupName</span></span>
<span data-ttu-id="dea3f-126">O grupo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dea3f-126">The resource group nam</span></span>

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

### <span data-ttu-id="dea3f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dea3f-127">-ResourceId</span></span>
<span data-ttu-id="dea3f-128">O recurso i</span><span class="sxs-lookup"><span data-stu-id="dea3f-128">The resource i</span></span>

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

### <span data-ttu-id="dea3f-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="dea3f-129">-ShortName</span></span>
<span data-ttu-id="dea3f-130">O nome curto do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="dea3f-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="dea3f-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="dea3f-131">-Tag</span></span>
<span data-ttu-id="dea3f-132">As marcas do grupo de ação resourc</span><span class="sxs-lookup"><span data-stu-id="dea3f-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="dea3f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dea3f-133">-Confirm</span></span>
<span data-ttu-id="dea3f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dea3f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dea3f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dea3f-135">-WhatIf</span></span>
<span data-ttu-id="dea3f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dea3f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dea3f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dea3f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dea3f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea3f-138">CommonParameters</span></span>
<span data-ttu-id="dea3f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dea3f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea3f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dea3f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea3f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dea3f-141">INPUTS</span></span>

### <span data-ttu-id="dea3f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dea3f-142">System.String</span></span>

### <span data-ttu-id="dea3f-143">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dea3f-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dea3f-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dea3f-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dea3f-145">System. Collections. Generic. IDictionary ' 2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dea3f-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dea3f-146">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="dea3f-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="dea3f-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dea3f-147">OUTPUTS</span></span>

### <span data-ttu-id="dea3f-148">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="dea3f-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="dea3f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dea3f-149">NOTES</span></span>

## <span data-ttu-id="dea3f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dea3f-150">RELATED LINKS</span></span>

<span data-ttu-id="dea3f-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="dea3f-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
