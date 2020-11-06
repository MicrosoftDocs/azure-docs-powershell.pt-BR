---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: bae9d8814d5988d0d509f64cb1de10040bb1af00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441275"
---
# <span data-ttu-id="77586-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="77586-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="77586-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77586-102">SYNOPSIS</span></span>
<span data-ttu-id="77586-103">Cria uma nova ou atualiza um grupo de ações existente.</span><span class="sxs-lookup"><span data-stu-id="77586-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77586-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77586-104">SYNTAX</span></span>

### <span data-ttu-id="77586-105">ByPropertyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="77586-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77586-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="77586-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77586-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="77586-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77586-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77586-108">DESCRIPTION</span></span>
<span data-ttu-id="77586-109">O cmdlet **set-AzureRmActionGroup** cria um novo ou atualiza um grupo de ações existente</span><span class="sxs-lookup"><span data-stu-id="77586-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="77586-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77586-110">EXAMPLES</span></span>

### <span data-ttu-id="77586-111">Exemplo 1: criar um grupo de ação</span><span class="sxs-lookup"><span data-stu-id="77586-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="77586-112">Os dois primeiros comandos criam dois destinatários.</span><span class="sxs-lookup"><span data-stu-id="77586-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="77586-113">O comando final cria um grupo de ação incluindo os dois destinatários.</span><span class="sxs-lookup"><span data-stu-id="77586-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="77586-114">OS</span><span class="sxs-lookup"><span data-stu-id="77586-114">PARAMETERS</span></span>

### <span data-ttu-id="77586-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77586-115">-DefaultProfile</span></span>
<span data-ttu-id="77586-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="77586-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77586-117">-Desativar o</span><span class="sxs-lookup"><span data-stu-id="77586-117">-DisableGroup</span></span>
<span data-ttu-id="77586-118">Desabilita o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="77586-118">Disables the action group.</span></span>

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

### <span data-ttu-id="77586-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77586-119">-InputObject</span></span>
<span data-ttu-id="77586-120">O grupo de ação resourc</span><span class="sxs-lookup"><span data-stu-id="77586-120">The action group resourc</span></span>

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

### <span data-ttu-id="77586-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="77586-121">-Name</span></span>
<span data-ttu-id="77586-122">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="77586-122">The name of the action group.</span></span>

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

### <span data-ttu-id="77586-123">-Receptor</span><span class="sxs-lookup"><span data-stu-id="77586-123">-Receiver</span></span>
<span data-ttu-id="77586-124">A lista de destinatários do grupo ação.</span><span class="sxs-lookup"><span data-stu-id="77586-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="77586-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77586-125">-ResourceGroupName</span></span>
<span data-ttu-id="77586-126">O grupo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="77586-126">The resource group nam</span></span>

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

### <span data-ttu-id="77586-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77586-127">-ResourceId</span></span>
<span data-ttu-id="77586-128">O recurso i</span><span class="sxs-lookup"><span data-stu-id="77586-128">The resource i</span></span>

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

### <span data-ttu-id="77586-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="77586-129">-ShortName</span></span>
<span data-ttu-id="77586-130">O nome curto do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="77586-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="77586-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="77586-131">-Tag</span></span>
<span data-ttu-id="77586-132">As marcas do grupo de ação resourc</span><span class="sxs-lookup"><span data-stu-id="77586-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="77586-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="77586-133">-Confirm</span></span>
<span data-ttu-id="77586-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77586-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77586-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77586-135">-WhatIf</span></span>
<span data-ttu-id="77586-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77586-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77586-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77586-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77586-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77586-138">CommonParameters</span></span>
<span data-ttu-id="77586-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77586-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77586-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77586-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77586-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77586-141">INPUTS</span></span>

### <span data-ttu-id="77586-142">System. String</span><span class="sxs-lookup"><span data-stu-id="77586-142">System.String</span></span>

### <span data-ttu-id="77586-143">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. Commands. insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="77586-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="77586-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77586-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="77586-145">System. Collections. Generic. IDictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="77586-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="77586-146">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="77586-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="77586-147">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77586-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="77586-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77586-148">OUTPUTS</span></span>

### <span data-ttu-id="77586-149">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="77586-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="77586-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77586-150">NOTES</span></span>

## <span data-ttu-id="77586-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77586-151">RELATED LINKS</span></span>

<span data-ttu-id="77586-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="77586-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
