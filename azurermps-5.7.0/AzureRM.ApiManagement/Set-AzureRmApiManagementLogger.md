---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 16a60f5f9951aaa40ac8da8584e1c2690206cdb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440894"
---
# <span data-ttu-id="51248-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="51248-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="51248-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51248-102">SYNOPSIS</span></span>
<span data-ttu-id="51248-103">Modifica um agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="51248-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51248-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51248-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51248-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51248-105">DESCRIPTION</span></span>
<span data-ttu-id="51248-106">O cmdlet **set-AzureRmApiManagementLogger** modifica as configurações de um **agente** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="51248-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="51248-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51248-107">EXAMPLES</span></span>

### <span data-ttu-id="51248-108">Exemplo 1: modificar um agente de log</span><span class="sxs-lookup"><span data-stu-id="51248-108">Example 1: Modify a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="51248-109">Esse comando modifica um logger que tem a ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="51248-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="51248-110">OS</span><span class="sxs-lookup"><span data-stu-id="51248-110">PARAMETERS</span></span>

### <span data-ttu-id="51248-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="51248-111">-ConnectionString</span></span>
<span data-ttu-id="51248-112">Especifica uma cadeia de conexão de hubs de eventos do Azure que inclui direitos de política de envio.</span><span class="sxs-lookup"><span data-stu-id="51248-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51248-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="51248-113">-Context</span></span>
<span data-ttu-id="51248-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="51248-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51248-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51248-115">-DefaultProfile</span></span>
<span data-ttu-id="51248-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51248-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51248-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="51248-117">-Description</span></span>
<span data-ttu-id="51248-118">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="51248-118">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51248-119">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="51248-119">-IsBuffered</span></span>
<span data-ttu-id="51248-120">Especifica que os registros no logger são armazenados em buffer antes da publicação.</span><span class="sxs-lookup"><span data-stu-id="51248-120">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="51248-121">Quando os registros são armazenados em buffer, eles são enviados para hubs de eventos a cada 15 segundos ou sempre que o buffer recebe 256 KB de mensagens.</span><span class="sxs-lookup"><span data-stu-id="51248-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51248-122">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="51248-122">-LoggerId</span></span>
<span data-ttu-id="51248-123">Especifica a ID do agente a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="51248-123">Specifies the ID of the logger to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51248-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="51248-124">-Name</span></span>
<span data-ttu-id="51248-125">Especifica o nome da entidade de um hub de eventos do portal clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="51248-125">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51248-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51248-126">-PassThru</span></span>
<span data-ttu-id="51248-127">Indica que esse cmdlet retorna o  **PsApiManagementLogger** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="51248-127">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51248-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51248-128">CommonParameters</span></span>
<span data-ttu-id="51248-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51248-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51248-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51248-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51248-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51248-131">INPUTS</span></span>

### <span data-ttu-id="51248-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="51248-132">None</span></span>
<span data-ttu-id="51248-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="51248-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51248-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51248-134">OUTPUTS</span></span>

### <span data-ttu-id="51248-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="51248-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="51248-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51248-136">NOTES</span></span>

## <span data-ttu-id="51248-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51248-137">RELATED LINKS</span></span>

[<span data-ttu-id="51248-138">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="51248-138">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="51248-139">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="51248-139">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="51248-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="51248-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


