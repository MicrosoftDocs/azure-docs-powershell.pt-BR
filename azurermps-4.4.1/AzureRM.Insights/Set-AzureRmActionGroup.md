---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: 29ef822e61c13d3ea976002c465a7c114296da9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432620"
---
# <span data-ttu-id="9d2d7-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9d2d7-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="9d2d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d2d7-102">SYNOPSIS</span></span>
<span data-ttu-id="9d2d7-103">Cria uma nova ou atualiza um grupo de ações existente.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d2d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d2d7-104">SYNTAX</span></span>

### <span data-ttu-id="9d2d7-105">ByPropertyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d2d7-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d2d7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d2d7-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d2d7-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9d2d7-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d2d7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d2d7-108">DESCRIPTION</span></span>
<span data-ttu-id="9d2d7-109">O cmdlet **set-AzureRmActionGroup** cria um novo ou atualiza um grupo de ações existente</span><span class="sxs-lookup"><span data-stu-id="9d2d7-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="9d2d7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d2d7-110">EXAMPLES</span></span>

### <span data-ttu-id="9d2d7-111">Exemplo 1: criar um grupo de ação</span><span class="sxs-lookup"><span data-stu-id="9d2d7-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="9d2d7-112">Os dois primeiros comandos criam dois destinatários.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="9d2d7-113">O comando final cria um grupo de ação incluindo os dois destinatários.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="9d2d7-114">OS</span><span class="sxs-lookup"><span data-stu-id="9d2d7-114">PARAMETERS</span></span>

### <span data-ttu-id="9d2d7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d2d7-115">-Name</span></span>
<span data-ttu-id="9d2d7-116">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-116">The name of the action group.</span></span>

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

### <span data-ttu-id="9d2d7-117">-ShortName</span><span class="sxs-lookup"><span data-stu-id="9d2d7-117">-ShortName</span></span>
<span data-ttu-id="9d2d7-118">O nome curto do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-118">The short name of the action group.</span></span>

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

### <span data-ttu-id="9d2d7-119">-Receptor</span><span class="sxs-lookup"><span data-stu-id="9d2d7-119">-Receiver</span></span>
<span data-ttu-id="9d2d7-120">A lista de destinatários do grupo ação.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-120">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="9d2d7-121">-Desativar o</span><span class="sxs-lookup"><span data-stu-id="9d2d7-121">-DisableGroup</span></span>
<span data-ttu-id="9d2d7-122">Desabilita o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-122">Disables the action group.</span></span>

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

### <span data-ttu-id="9d2d7-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d2d7-123">-Confirm</span></span>
<span data-ttu-id="9d2d7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d2d7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d2d7-125">-DefaultProfile</span></span>
<span data-ttu-id="9d2d7-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d2d7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d2d7-127">-InputObject</span></span>
<span data-ttu-id="9d2d7-128">O recurso grupo de ações</span><span class="sxs-lookup"><span data-stu-id="9d2d7-128">The action group resource</span></span>

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

### <span data-ttu-id="9d2d7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d2d7-129">-ResourceGroupName</span></span>
<span data-ttu-id="9d2d7-130">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9d2d7-130">The resource group name</span></span>

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

### <span data-ttu-id="9d2d7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d2d7-131">-ResourceId</span></span>
<span data-ttu-id="9d2d7-132">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="9d2d7-132">The resource id</span></span>

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

### <span data-ttu-id="9d2d7-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="9d2d7-133">-Tag</span></span>
<span data-ttu-id="9d2d7-134">As marcas do recurso de grupo de ação</span><span class="sxs-lookup"><span data-stu-id="9d2d7-134">The tags of the action group resource</span></span>

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

### <span data-ttu-id="9d2d7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d2d7-135">-WhatIf</span></span>
<span data-ttu-id="9d2d7-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d2d7-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d2d7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d2d7-138">CommonParameters</span></span>
<span data-ttu-id="9d2d7-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d2d7-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d2d7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d2d7-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d2d7-141">INPUTS</span></span>

## <span data-ttu-id="9d2d7-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d2d7-142">OUTPUTS</span></span>

### <span data-ttu-id="9d2d7-143">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="9d2d7-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="9d2d7-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d2d7-144">NOTES</span></span>

## <span data-ttu-id="9d2d7-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d2d7-145">RELATED LINKS</span></span>

<span data-ttu-id="9d2d7-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="9d2d7-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
