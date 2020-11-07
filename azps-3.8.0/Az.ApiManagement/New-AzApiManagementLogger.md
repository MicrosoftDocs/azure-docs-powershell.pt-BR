---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: 211677c8e6fc12fa857d9b9da8653eadcea8b10c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942224"
---
# <span data-ttu-id="476ee-101">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="476ee-101">New-AzApiManagementLogger</span></span>

## <span data-ttu-id="476ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="476ee-102">SYNOPSIS</span></span>
<span data-ttu-id="476ee-103">Cria um agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="476ee-103">Creates an API Management Logger.</span></span>

## <span data-ttu-id="476ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="476ee-104">SYNTAX</span></span>

### <span data-ttu-id="476ee-105">EventHubLoggerSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="476ee-105">EventHubLoggerSet (Default)</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="476ee-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="476ee-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="476ee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="476ee-107">DESCRIPTION</span></span>
<span data-ttu-id="476ee-108">O cmdlet **New-AzApiManagementLogger** cria um **agente** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="476ee-108">The **New-AzApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="476ee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="476ee-109">EXAMPLES</span></span>

### <span data-ttu-id="476ee-110">Exemplo 1: criar um agente de log</span><span class="sxs-lookup"><span data-stu-id="476ee-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="476ee-111">Esse comando cria um logger chamado ContosoSdkEventHub usando a cadeia de conexão especificada.</span><span class="sxs-lookup"><span data-stu-id="476ee-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="476ee-112">OS</span><span class="sxs-lookup"><span data-stu-id="476ee-112">PARAMETERS</span></span>

### <span data-ttu-id="476ee-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="476ee-113">-ConnectionString</span></span>
<span data-ttu-id="476ee-114">Especifica uma cadeia de conexão de hubs de eventos do Azure que começa com o seguinte: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="476ee-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="476ee-115">A chave com direitos de envio na cadeia de conexão deve ser configurada.</span><span class="sxs-lookup"><span data-stu-id="476ee-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="476ee-116">-Context</span></span>
<span data-ttu-id="476ee-117">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="476ee-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476ee-118">-DefaultProfile</span></span>
<span data-ttu-id="476ee-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="476ee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="476ee-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="476ee-120">-Description</span></span>
<span data-ttu-id="476ee-121">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="476ee-121">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="476ee-122">-InstrumentationKey</span></span>
<span data-ttu-id="476ee-123">Chave de instrumentação dos insights do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="476ee-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="476ee-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="476ee-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-125">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="476ee-125">-IsBuffered</span></span>
<span data-ttu-id="476ee-126">Especifica se os registros no logger são armazenados em buffer antes da publicação.</span><span class="sxs-lookup"><span data-stu-id="476ee-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="476ee-127">O valor padrão é $True.</span><span class="sxs-lookup"><span data-stu-id="476ee-127">The default value is $True.</span></span>
<span data-ttu-id="476ee-128">Quando os registros são armazenados em buffer, eles são enviados para hubs de eventos a cada 15 segundos ou sempre que o buffer recebe 256 KB de mensagens.</span><span class="sxs-lookup"><span data-stu-id="476ee-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-129">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="476ee-129">-LoggerId</span></span>
<span data-ttu-id="476ee-130">Especifica uma ID para o agente de log.</span><span class="sxs-lookup"><span data-stu-id="476ee-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="476ee-131">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="476ee-131">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="476ee-132">-Name</span></span>
<span data-ttu-id="476ee-133">Especifica o nome da entidade de um hub de eventos do portal clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="476ee-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476ee-134">CommonParameters</span></span>
<span data-ttu-id="476ee-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476ee-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="476ee-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476ee-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="476ee-137">INPUTS</span></span>

### <span data-ttu-id="476ee-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="476ee-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="476ee-139">System. String</span><span class="sxs-lookup"><span data-stu-id="476ee-139">System.String</span></span>

### <span data-ttu-id="476ee-140">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="476ee-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="476ee-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="476ee-141">OUTPUTS</span></span>

### <span data-ttu-id="476ee-142">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="476ee-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="476ee-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="476ee-143">NOTES</span></span>

## <span data-ttu-id="476ee-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="476ee-144">RELATED LINKS</span></span>

[<span data-ttu-id="476ee-145">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="476ee-145">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="476ee-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="476ee-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="476ee-147">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="476ee-147">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


