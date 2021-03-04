---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: 1dbdbc6a616e9903c6a79192d089ea959835a9f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890464"
---
# <span data-ttu-id="44e7e-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="44e7e-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="44e7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="44e7e-103">Vincula um Hub de Notificação do Azure a esse serviço de comunicação.</span><span class="sxs-lookup"><span data-stu-id="44e7e-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="44e7e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="44e7e-104">SYNTAX</span></span>

### <span data-ttu-id="44e7e-105">LinkExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44e7e-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44e7e-106">Link</span><span class="sxs-lookup"><span data-stu-id="44e7e-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44e7e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="44e7e-107">DESCRIPTION</span></span>
<span data-ttu-id="44e7e-108">Vincula um Hub de Notificação do Azure a esse serviço de comunicação.</span><span class="sxs-lookup"><span data-stu-id="44e7e-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="44e7e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44e7e-109">EXAMPLES</span></span>

### <span data-ttu-id="44e7e-110">Exemplo 1: Fornecer detalhes do Hub de Notificação interativamente</span><span class="sxs-lookup"><span data-stu-id="44e7e-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="44e7e-111">Um hub de notificação vinculado permite que um recurso do ACS envie notificações para determinados eventos.</span><span class="sxs-lookup"><span data-stu-id="44e7e-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="44e7e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="44e7e-112">PARAMETERS</span></span>

### <span data-ttu-id="44e7e-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="44e7e-113">-CommunicationServiceName</span></span>
<span data-ttu-id="44e7e-114">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="44e7e-114">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e7e-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="44e7e-115">-ConnectionString</span></span>
<span data-ttu-id="44e7e-116">Cadeia de conexão para o hub de notificação</span><span class="sxs-lookup"><span data-stu-id="44e7e-116">Connection string for the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e7e-117">-DefaultProfile</span></span>
<span data-ttu-id="44e7e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44e7e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e7e-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="44e7e-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="44e7e-120">Descrição de um Hub de Notificação do Azure para vincular ao serviço de comunicação Para construir, consulte a seção NOTES para propriedades LINKNOTIFICATIONHUBPARAMETER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="44e7e-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44e7e-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="44e7e-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="44e7e-122">A ID do recurso do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="44e7e-122">The resource ID of the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e7e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44e7e-123">-ResourceGroupName</span></span>
<span data-ttu-id="44e7e-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="44e7e-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="44e7e-125">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="44e7e-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e7e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44e7e-126">-SubscriptionId</span></span>
<span data-ttu-id="44e7e-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44e7e-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="44e7e-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="44e7e-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e7e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44e7e-129">-Confirm</span></span>
<span data-ttu-id="44e7e-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44e7e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44e7e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44e7e-131">-WhatIf</span></span>
<span data-ttu-id="44e7e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44e7e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44e7e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44e7e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44e7e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e7e-134">CommonParameters</span></span>
<span data-ttu-id="44e7e-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44e7e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e7e-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44e7e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e7e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44e7e-137">INPUTS</span></span>

### <span data-ttu-id="44e7e-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="44e7e-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="44e7e-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="44e7e-139">OUTPUTS</span></span>

### <span data-ttu-id="44e7e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="44e7e-140">System.String</span></span>

## <span data-ttu-id="44e7e-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="44e7e-141">NOTES</span></span>

<span data-ttu-id="44e7e-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="44e7e-142">ALIASES</span></span>

<span data-ttu-id="44e7e-143">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="44e7e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44e7e-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="44e7e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44e7e-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44e7e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44e7e-146">LINKNOTIFICATIONHUBPARAMETER : Descrição de um Hub de Notificação <ILinkNotificationHubParameters> do Azure para vincular ao serviço de comunicação</span><span class="sxs-lookup"><span data-stu-id="44e7e-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="44e7e-147">`ConnectionString <String>`: Cadeia de conexão para o hub de notificação</span><span class="sxs-lookup"><span data-stu-id="44e7e-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="44e7e-148">`ResourceId <String>`: A ID do recurso do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="44e7e-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="44e7e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44e7e-149">RELATED LINKS</span></span>

