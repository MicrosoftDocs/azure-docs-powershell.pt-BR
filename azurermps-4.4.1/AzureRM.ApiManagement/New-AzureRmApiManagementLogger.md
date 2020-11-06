---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: c7827f0df8b1baf4bb2fead9df091619751c969c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431222"
---
# <span data-ttu-id="6e01a-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e01a-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="6e01a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e01a-102">SYNOPSIS</span></span>
<span data-ttu-id="6e01a-103">Cria um agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="6e01a-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e01a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e01a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e01a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e01a-105">DESCRIPTION</span></span>
<span data-ttu-id="6e01a-106">O cmdlet **New-AzureRmApiManagementLogger** cria um **agente** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e01a-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="6e01a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e01a-107">EXAMPLES</span></span>

### <span data-ttu-id="6e01a-108">Exemplo 1: criar um agente de log</span><span class="sxs-lookup"><span data-stu-id="6e01a-108">Example 1: Create a logger</span></span>
```
PS C:\>New-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="6e01a-109">Esse comando cria um logger chamado ContosoSdkEventHub usando a cadeia de conexão especificada.</span><span class="sxs-lookup"><span data-stu-id="6e01a-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="6e01a-110">OS</span><span class="sxs-lookup"><span data-stu-id="6e01a-110">PARAMETERS</span></span>

### <span data-ttu-id="6e01a-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6e01a-111">-ConnectionString</span></span>
<span data-ttu-id="6e01a-112">Especifica uma cadeia de conexão de hubs de eventos do Azure que começa com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6e01a-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="6e01a-113">A chave com direitos de envio na cadeia de conexão deve ser configurada.</span><span class="sxs-lookup"><span data-stu-id="6e01a-113">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="6e01a-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6e01a-114">-Context</span></span>
<span data-ttu-id="6e01a-115">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6e01a-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6e01a-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6e01a-116">-Description</span></span>
<span data-ttu-id="6e01a-117">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="6e01a-117">Specifies a description.</span></span>

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

### <span data-ttu-id="6e01a-118">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="6e01a-118">-IsBuffered</span></span>
<span data-ttu-id="6e01a-119">Especifica se os registros no logger são armazenados em buffer antes da publicação.</span><span class="sxs-lookup"><span data-stu-id="6e01a-119">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="6e01a-120">O valor padrão é $True.</span><span class="sxs-lookup"><span data-stu-id="6e01a-120">The default value is $True.</span></span>
<span data-ttu-id="6e01a-121">Quando os registros são armazenados em buffer, eles são enviados para hubs de eventos a cada 15 segundos ou sempre que o buffer recebe 256 KB de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6e01a-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e01a-122">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="6e01a-122">-LoggerId</span></span>
<span data-ttu-id="6e01a-123">Especifica uma ID para o agente de log.</span><span class="sxs-lookup"><span data-stu-id="6e01a-123">Specifies an ID for the logger.</span></span>
<span data-ttu-id="6e01a-124">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="6e01a-124">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="6e01a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e01a-125">-Name</span></span>
<span data-ttu-id="6e01a-126">Especifica o nome da entidade de um hub de eventos do portal clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e01a-126">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="6e01a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e01a-127">-DefaultProfile</span></span>
<span data-ttu-id="6e01a-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e01a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e01a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e01a-129">CommonParameters</span></span>
<span data-ttu-id="6e01a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e01a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e01a-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e01a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e01a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e01a-132">INPUTS</span></span>

## <span data-ttu-id="6e01a-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e01a-133">OUTPUTS</span></span>

### <span data-ttu-id="6e01a-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e01a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="6e01a-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e01a-135">NOTES</span></span>

## <span data-ttu-id="6e01a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e01a-136">RELATED LINKS</span></span>

[<span data-ttu-id="6e01a-137">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e01a-137">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="6e01a-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e01a-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="6e01a-139">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e01a-139">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


