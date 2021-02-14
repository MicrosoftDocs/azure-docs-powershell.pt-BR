---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111164"
---
# <span data-ttu-id="d9f8d-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d9f8d-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="d9f8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f8d-103">Vincula um Hub de Notificação do Azure a este serviço de comunicação.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="d9f8d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9f8d-104">SYNTAX</span></span>

### <span data-ttu-id="d9f8d-105">LinkExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d9f8d-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d9f8d-106">Link</span><span class="sxs-lookup"><span data-stu-id="d9f8d-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9f8d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9f8d-107">DESCRIPTION</span></span>
<span data-ttu-id="d9f8d-108">Vincula um Hub de Notificação do Azure a este serviço de comunicação.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="d9f8d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d9f8d-109">EXAMPLES</span></span>

### <span data-ttu-id="d9f8d-110">Exemplo 1: fornecer detalhes do Hub de Notificação interativamente</span><span class="sxs-lookup"><span data-stu-id="d9f8d-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="d9f8d-111">Um hub de notificação vinculado permite que um recurso ACS envie notificações para determinados eventos.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="d9f8d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9f8d-112">PARAMETERS</span></span>

### <span data-ttu-id="d9f8d-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="d9f8d-113">-CommunicationServiceName</span></span>
<span data-ttu-id="d9f8d-114">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-114">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="d9f8d-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d9f8d-115">-ConnectionString</span></span>
<span data-ttu-id="d9f8d-116">Cadeia de conexão do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="d9f8d-116">Connection string for the notification hub</span></span>

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

### <span data-ttu-id="d9f8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f8d-117">-DefaultProfile</span></span>
<span data-ttu-id="d9f8d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9f8d-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="d9f8d-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="d9f8d-120">Descrição de um Hub de Notificação do Azure para vincular ao serviço de comunicação Para construir, consulte a seção ANOTAÇÕES para propriedades LINKNOTIFICATIONHUBPARAMETER e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="d9f8d-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d9f8d-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="d9f8d-122">A ID do recurso do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="d9f8d-122">The resource ID of the notification hub</span></span>

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

### <span data-ttu-id="d9f8d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f8d-123">-ResourceGroupName</span></span>
<span data-ttu-id="d9f8d-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d9f8d-125">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d9f8d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9f8d-126">-SubscriptionId</span></span>
<span data-ttu-id="d9f8d-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9f8d-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9f8d-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d9f8d-129">-Confirm</span></span>
<span data-ttu-id="d9f8d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f8d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9f8d-131">-WhatIf</span></span>
<span data-ttu-id="d9f8d-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9f8d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9f8d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f8d-134">CommonParameters</span></span>
<span data-ttu-id="d9f8d-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f8d-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9f8d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f8d-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="d9f8d-137">INPUTS</span></span>

### <span data-ttu-id="d9f8d-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="d9f8d-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="d9f8d-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="d9f8d-139">OUTPUTS</span></span>

### <span data-ttu-id="d9f8d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d9f8d-140">System.String</span></span>

## <span data-ttu-id="d9f8d-141">Notas</span><span class="sxs-lookup"><span data-stu-id="d9f8d-141">NOTES</span></span>

<span data-ttu-id="d9f8d-142">Aliases</span><span class="sxs-lookup"><span data-stu-id="d9f8d-142">ALIASES</span></span>

<span data-ttu-id="d9f8d-143">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="d9f8d-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d9f8d-144">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9f8d-145">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9f8d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d9f8d-146">LINKNOTIFICATIONHUBPARAMETER : Descrição de um Hub de Notificação do <ILinkNotificationHubParameters> Azure para vincular ao serviço de comunicação</span><span class="sxs-lookup"><span data-stu-id="d9f8d-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="d9f8d-147">`ConnectionString <String>`: cadeia de conexão do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="d9f8d-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="d9f8d-148">`ResourceId <String>`: A ID do recurso do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="d9f8d-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="d9f8d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9f8d-149">RELATED LINKS</span></span>

