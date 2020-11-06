---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2929cbd89328d971b47b748d4aa042ade13c1af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429906"
---
# <span data-ttu-id="eff25-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="eff25-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="eff25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eff25-102">SYNOPSIS</span></span>
<span data-ttu-id="eff25-103">Cria um agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="eff25-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eff25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eff25-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eff25-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eff25-105">DESCRIPTION</span></span>
<span data-ttu-id="eff25-106">O cmdlet **New-AzureRmApiManagementLogger** cria um **agente** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="eff25-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="eff25-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eff25-107">EXAMPLES</span></span>

### <span data-ttu-id="eff25-108">Exemplo 1: criar um agente de log</span><span class="sxs-lookup"><span data-stu-id="eff25-108">Example 1: Create a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="eff25-109">Esse comando cria um logger chamado ContosoSdkEventHub usando a cadeia de conexão especificada.</span><span class="sxs-lookup"><span data-stu-id="eff25-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="eff25-110">OS</span><span class="sxs-lookup"><span data-stu-id="eff25-110">PARAMETERS</span></span>

### <span data-ttu-id="eff25-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="eff25-111">-ConnectionString</span></span>
<span data-ttu-id="eff25-112">Especifica uma cadeia de conexão de hubs de eventos do Azure que começa com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="eff25-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="eff25-113">A chave com direitos de envio na cadeia de conexão deve ser configurada.</span><span class="sxs-lookup"><span data-stu-id="eff25-113">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="eff25-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="eff25-114">-Context</span></span>
<span data-ttu-id="eff25-115">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="eff25-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eff25-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff25-116">-DefaultProfile</span></span>
<span data-ttu-id="eff25-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eff25-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="eff25-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="eff25-118">-Description</span></span>
<span data-ttu-id="eff25-119">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="eff25-119">Specifies a description.</span></span>

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

### <span data-ttu-id="eff25-120">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="eff25-120">-IsBuffered</span></span>
<span data-ttu-id="eff25-121">Especifica se os registros no logger são armazenados em buffer antes da publicação.</span><span class="sxs-lookup"><span data-stu-id="eff25-121">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="eff25-122">O valor padrão é $True.</span><span class="sxs-lookup"><span data-stu-id="eff25-122">The default value is $True.</span></span>
<span data-ttu-id="eff25-123">Quando os registros são armazenados em buffer, eles são enviados para hubs de eventos a cada 15 segundos ou sempre que o buffer recebe 256 KB de mensagens.</span><span class="sxs-lookup"><span data-stu-id="eff25-123">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eff25-124">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="eff25-124">-LoggerId</span></span>
<span data-ttu-id="eff25-125">Especifica uma ID para o agente de log.</span><span class="sxs-lookup"><span data-stu-id="eff25-125">Specifies an ID for the logger.</span></span>
<span data-ttu-id="eff25-126">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="eff25-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="eff25-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="eff25-127">-Name</span></span>
<span data-ttu-id="eff25-128">Especifica o nome da entidade de um hub de eventos do portal clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="eff25-128">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="eff25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff25-129">CommonParameters</span></span>
<span data-ttu-id="eff25-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff25-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff25-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff25-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eff25-132">INPUTS</span></span>

### <span data-ttu-id="eff25-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="eff25-133">None</span></span>
<span data-ttu-id="eff25-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="eff25-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eff25-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eff25-135">OUTPUTS</span></span>

### <span data-ttu-id="eff25-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="eff25-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="eff25-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eff25-137">NOTES</span></span>

## <span data-ttu-id="eff25-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eff25-138">RELATED LINKS</span></span>

[<span data-ttu-id="eff25-139">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="eff25-139">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="eff25-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="eff25-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="eff25-141">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="eff25-141">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


