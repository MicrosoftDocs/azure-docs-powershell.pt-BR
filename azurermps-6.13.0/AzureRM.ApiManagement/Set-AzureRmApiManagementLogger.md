---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 7a037b107f3d72a000c2f69c8de507a4f414e283
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429611"
---
# <span data-ttu-id="e11b5-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e11b5-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="e11b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e11b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e11b5-103">Modifica um agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e11b5-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e11b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e11b5-104">SYNTAX</span></span>

### <span data-ttu-id="e11b5-105">EventHubLoggerSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e11b5-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e11b5-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="e11b5-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-InstrumentationKey <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e11b5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e11b5-107">DESCRIPTION</span></span>
<span data-ttu-id="e11b5-108">O cmdlet **set-AzureRmApiManagementLogger** modifica as configurações de um **agente** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="e11b5-108">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="e11b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e11b5-109">EXAMPLES</span></span>

### <span data-ttu-id="e11b5-110">Exemplo 1: modificar o agente do EventHub</span><span class="sxs-lookup"><span data-stu-id="e11b5-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="e11b5-111">Esse comando modifica um logger que tem a ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="e11b5-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="e11b5-112">OS</span><span class="sxs-lookup"><span data-stu-id="e11b5-112">PARAMETERS</span></span>

### <span data-ttu-id="e11b5-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e11b5-113">-ConnectionString</span></span>
<span data-ttu-id="e11b5-114">Especifica uma cadeia de conexão de hubs de eventos do Azure que inclui direitos de política de envio.</span><span class="sxs-lookup"><span data-stu-id="e11b5-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="e11b5-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e11b5-115">-Context</span></span>
<span data-ttu-id="e11b5-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e11b5-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e11b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e11b5-117">-DefaultProfile</span></span>
<span data-ttu-id="e11b5-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e11b5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e11b5-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e11b5-119">-Description</span></span>
<span data-ttu-id="e11b5-120">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="e11b5-120">Specifies a description.</span></span>

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

### <span data-ttu-id="e11b5-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="e11b5-121">-InstrumentationKey</span></span>
<span data-ttu-id="e11b5-122">Chave de instrumentação dos insights do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e11b5-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="e11b5-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e11b5-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="e11b5-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="e11b5-124">-IsBuffered</span></span>
<span data-ttu-id="e11b5-125">Especifica que os registros no logger são armazenados em buffer antes da publicação.</span><span class="sxs-lookup"><span data-stu-id="e11b5-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="e11b5-126">Quando os registros são armazenados em buffer, eles são enviados para hubs de eventos a cada 15 segundos ou sempre que o buffer recebe 256 KB de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e11b5-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="e11b5-127">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="e11b5-127">-LoggerId</span></span>
<span data-ttu-id="e11b5-128">Especifica a ID do agente a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e11b5-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="e11b5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e11b5-129">-Name</span></span>
<span data-ttu-id="e11b5-130">Especifica o nome da entidade de um hub de eventos do portal clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="e11b5-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="e11b5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e11b5-131">-PassThru</span></span>
<span data-ttu-id="e11b5-132">Indica que esse cmdlet retorna o  **PsApiManagementLogger** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e11b5-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e11b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e11b5-133">CommonParameters</span></span>
<span data-ttu-id="e11b5-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e11b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e11b5-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e11b5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e11b5-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e11b5-136">INPUTS</span></span>

### <span data-ttu-id="e11b5-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e11b5-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e11b5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e11b5-138">System.String</span></span>

### <span data-ttu-id="e11b5-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e11b5-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e11b5-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e11b5-140">OUTPUTS</span></span>

### <span data-ttu-id="e11b5-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e11b5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="e11b5-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e11b5-142">NOTES</span></span>

## <span data-ttu-id="e11b5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e11b5-143">RELATED LINKS</span></span>

[<span data-ttu-id="e11b5-144">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e11b5-144">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="e11b5-145">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e11b5-145">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="e11b5-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e11b5-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


