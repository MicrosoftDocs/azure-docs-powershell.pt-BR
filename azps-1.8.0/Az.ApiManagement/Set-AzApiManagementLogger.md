---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 4c7f4b4f308d04c6f9c82e70f9fbe0598bd4a9fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771334"
---
# <span data-ttu-id="80e43-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80e43-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="80e43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80e43-102">SYNOPSIS</span></span>
<span data-ttu-id="80e43-103">Modifica um agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="80e43-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="80e43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80e43-104">SYNTAX</span></span>

### <span data-ttu-id="80e43-105">EventHubLoggerSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="80e43-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80e43-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="80e43-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80e43-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80e43-107">DESCRIPTION</span></span>
<span data-ttu-id="80e43-108">O cmdlet **set-AzApiManagementLogger** modifica as configurações de um **agente** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="80e43-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="80e43-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80e43-109">EXAMPLES</span></span>

### <span data-ttu-id="80e43-110">Exemplo 1: modificar o agente do EventHub</span><span class="sxs-lookup"><span data-stu-id="80e43-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="80e43-111">Esse comando modifica um logger que tem a ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="80e43-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="80e43-112">OS</span><span class="sxs-lookup"><span data-stu-id="80e43-112">PARAMETERS</span></span>

### <span data-ttu-id="80e43-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="80e43-113">-ConnectionString</span></span>
<span data-ttu-id="80e43-114">Especifica uma cadeia de conexão de hubs de eventos do Azure que inclui direitos de política de envio.</span><span class="sxs-lookup"><span data-stu-id="80e43-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e43-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="80e43-115">-Context</span></span>
<span data-ttu-id="80e43-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="80e43-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e43-117">-DefaultProfile</span></span>
<span data-ttu-id="80e43-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80e43-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80e43-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="80e43-119">-Description</span></span>
<span data-ttu-id="80e43-120">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="80e43-120">Specifies a description.</span></span>

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

### <span data-ttu-id="80e43-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="80e43-121">-InstrumentationKey</span></span>
<span data-ttu-id="80e43-122">Chave de instrumentação dos insights do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="80e43-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="80e43-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="80e43-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e43-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="80e43-124">-IsBuffered</span></span>
<span data-ttu-id="80e43-125">Especifica que os registros no logger são armazenados em buffer antes da publicação.</span><span class="sxs-lookup"><span data-stu-id="80e43-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="80e43-126">Quando os registros são armazenados em buffer, eles são enviados para hubs de eventos a cada 15 segundos ou sempre que o buffer recebe 256 KB de mensagens.</span><span class="sxs-lookup"><span data-stu-id="80e43-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e43-127">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="80e43-127">-LoggerId</span></span>
<span data-ttu-id="80e43-128">Especifica a ID do agente a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="80e43-128">Specifies the ID of the logger to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e43-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="80e43-129">-Name</span></span>
<span data-ttu-id="80e43-130">Especifica o nome da entidade de um hub de eventos do portal clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="80e43-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e43-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80e43-131">-PassThru</span></span>
<span data-ttu-id="80e43-132">Indica que esse cmdlet retorna o  **PsApiManagementLogger** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="80e43-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e43-133">CommonParameters</span></span>
<span data-ttu-id="80e43-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80e43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e43-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80e43-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e43-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80e43-136">INPUTS</span></span>

### <span data-ttu-id="80e43-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80e43-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80e43-138">System. String</span><span class="sxs-lookup"><span data-stu-id="80e43-138">System.String</span></span>

### <span data-ttu-id="80e43-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80e43-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80e43-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80e43-140">OUTPUTS</span></span>

### <span data-ttu-id="80e43-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80e43-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="80e43-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80e43-142">NOTES</span></span>

## <span data-ttu-id="80e43-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80e43-143">RELATED LINKS</span></span>

[<span data-ttu-id="80e43-144">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80e43-144">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="80e43-145">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80e43-145">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="80e43-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80e43-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


