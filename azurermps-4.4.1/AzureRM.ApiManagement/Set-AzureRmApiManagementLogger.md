---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: c21c227dd748f28523f4ac616d003e029d19e38f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431838"
---
# <span data-ttu-id="3a736-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3a736-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="3a736-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a736-102">SYNOPSIS</span></span>
<span data-ttu-id="3a736-103">Modifica um agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="3a736-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a736-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a736-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a736-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a736-105">DESCRIPTION</span></span>
<span data-ttu-id="3a736-106">O cmdlet **set-AzureRmApiManagementLogger** modifica as configurações de um **agente** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a736-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="3a736-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a736-107">EXAMPLES</span></span>

### <span data-ttu-id="3a736-108">Exemplo 1: modificar um agente de log</span><span class="sxs-lookup"><span data-stu-id="3a736-108">Example 1: Modify a logger</span></span>
```
PS C:\>Set-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="3a736-109">Esse comando modifica um logger que tem a ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="3a736-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="3a736-110">OS</span><span class="sxs-lookup"><span data-stu-id="3a736-110">PARAMETERS</span></span>

### <span data-ttu-id="3a736-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3a736-111">-ConnectionString</span></span>
<span data-ttu-id="3a736-112">Especifica uma cadeia de conexão de hubs de eventos do Azure que inclui direitos de política de envio.</span><span class="sxs-lookup"><span data-stu-id="3a736-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="3a736-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3a736-113">-Context</span></span>
<span data-ttu-id="3a736-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3a736-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3a736-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3a736-115">-Description</span></span>
<span data-ttu-id="3a736-116">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="3a736-116">Specifies a description.</span></span>

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

### <span data-ttu-id="3a736-117">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="3a736-117">-IsBuffered</span></span>
<span data-ttu-id="3a736-118">Especifica que os registros no logger são armazenados em buffer antes da publicação.</span><span class="sxs-lookup"><span data-stu-id="3a736-118">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="3a736-119">Quando os registros são armazenados em buffer, eles são enviados para hubs de eventos a cada 15 segundos ou sempre que o buffer recebe 256 KB de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3a736-119">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="3a736-120">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="3a736-120">-LoggerId</span></span>
<span data-ttu-id="3a736-121">Especifica a ID do agente a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="3a736-121">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="3a736-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a736-122">-Name</span></span>
<span data-ttu-id="3a736-123">Especifica o nome da entidade de um hub de eventos do portal clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a736-123">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="3a736-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a736-124">-PassThru</span></span>
<span data-ttu-id="3a736-125">Indica que esse cmdlet retorna o  **PsApiManagementLogger** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3a736-125">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3a736-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a736-126">-DefaultProfile</span></span>
<span data-ttu-id="3a736-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a736-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a736-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a736-128">CommonParameters</span></span>
<span data-ttu-id="3a736-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a736-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a736-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a736-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a736-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a736-131">INPUTS</span></span>

## <span data-ttu-id="3a736-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a736-132">OUTPUTS</span></span>

### <span data-ttu-id="3a736-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3a736-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="3a736-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a736-134">NOTES</span></span>

## <span data-ttu-id="3a736-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a736-135">RELATED LINKS</span></span>

[<span data-ttu-id="3a736-136">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3a736-136">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="3a736-137">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3a736-137">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="3a736-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3a736-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


