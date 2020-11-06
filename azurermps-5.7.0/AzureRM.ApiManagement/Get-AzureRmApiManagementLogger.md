---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: bcfcd052d2278fa39bc310a5c1927457a1b0fcd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432514"
---
# <span data-ttu-id="984b8-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="984b8-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="984b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="984b8-102">SYNOPSIS</span></span>
<span data-ttu-id="984b8-103">Obtém objetos de agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="984b8-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="984b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="984b8-104">SYNTAX</span></span>

### <span data-ttu-id="984b8-105">GetAllLoggers (padrão)</span><span class="sxs-lookup"><span data-stu-id="984b8-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="984b8-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="984b8-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="984b8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="984b8-107">DESCRIPTION</span></span>
<span data-ttu-id="984b8-108">O cmdlet **Get-AzureRmApiManagementLogger** Obtém um **agente** de gerenciamento de API do Azure ou todos os registradores.</span><span class="sxs-lookup"><span data-stu-id="984b8-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="984b8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="984b8-109">EXAMPLES</span></span>

### <span data-ttu-id="984b8-110">Exemplo 1: obter todos os registradores</span><span class="sxs-lookup"><span data-stu-id="984b8-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="984b8-111">Esse comando obtém todos os loggers do contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="984b8-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="984b8-112">Exemplo 2: obter um agente de log específico</span><span class="sxs-lookup"><span data-stu-id="984b8-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="984b8-113">Esse comando Remove um logger que tem a ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="984b8-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="984b8-114">OS</span><span class="sxs-lookup"><span data-stu-id="984b8-114">PARAMETERS</span></span>

### <span data-ttu-id="984b8-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="984b8-115">-Context</span></span>
<span data-ttu-id="984b8-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="984b8-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="984b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984b8-117">-DefaultProfile</span></span>
<span data-ttu-id="984b8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="984b8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="984b8-119">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="984b8-119">-LoggerId</span></span>
<span data-ttu-id="984b8-120">Especifica a ID do agente de log específico a obter.</span><span class="sxs-lookup"><span data-stu-id="984b8-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByLoggerId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="984b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984b8-121">CommonParameters</span></span>
<span data-ttu-id="984b8-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="984b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984b8-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="984b8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984b8-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="984b8-124">INPUTS</span></span>

### <span data-ttu-id="984b8-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="984b8-125">None</span></span>
<span data-ttu-id="984b8-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="984b8-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="984b8-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="984b8-127">OUTPUTS</span></span>

### <span data-ttu-id="984b8-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="984b8-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>
<span data-ttu-id="984b8-129">O detalhe do agente de log configurado no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="984b8-129">The detail of the Logger configured in API Management service.</span></span>

### <span data-ttu-id="984b8-130">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="984b8-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>
<span data-ttu-id="984b8-131">A lista de agentes configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="984b8-131">The list of Loggers configured in API Management service.</span></span>

## <span data-ttu-id="984b8-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="984b8-132">NOTES</span></span>

## <span data-ttu-id="984b8-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="984b8-133">RELATED LINKS</span></span>

[<span data-ttu-id="984b8-134">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="984b8-134">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="984b8-135">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="984b8-135">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="984b8-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="984b8-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


