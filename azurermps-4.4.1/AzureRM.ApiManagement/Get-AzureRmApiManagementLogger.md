---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432689"
---
# <span data-ttu-id="a8206-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a8206-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="a8206-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8206-102">SYNOPSIS</span></span>
<span data-ttu-id="a8206-103">Obtém objetos de agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a8206-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8206-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8206-104">SYNTAX</span></span>

### <span data-ttu-id="a8206-105">Obter todos os registradores (padrão)</span><span class="sxs-lookup"><span data-stu-id="a8206-105">Get all loggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8206-106">Obter por ID do logger</span><span class="sxs-lookup"><span data-stu-id="a8206-106">Get by logger ID</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8206-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8206-107">DESCRIPTION</span></span>
<span data-ttu-id="a8206-108">O cmdlet **Get-AzureRmApiManagementLogger** Obtém um **agente** de gerenciamento de API do Azure ou todos os registradores.</span><span class="sxs-lookup"><span data-stu-id="a8206-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="a8206-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8206-109">EXAMPLES</span></span>

### <span data-ttu-id="a8206-110">Exemplo 1: obter todos os registradores</span><span class="sxs-lookup"><span data-stu-id="a8206-110">Example 1: Get all loggers</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

<span data-ttu-id="a8206-111">Esse comando obtém todos os loggers do contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="a8206-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="a8206-112">Exemplo 2: obter um agente de log específico</span><span class="sxs-lookup"><span data-stu-id="a8206-112">Example 2: Get a specific logger</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

<span data-ttu-id="a8206-113">Esse comando Remove um logger que tem a ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="a8206-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="a8206-114">OS</span><span class="sxs-lookup"><span data-stu-id="a8206-114">PARAMETERS</span></span>

### <span data-ttu-id="a8206-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a8206-115">-Context</span></span>
<span data-ttu-id="a8206-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a8206-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a8206-117">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="a8206-117">-LoggerId</span></span>
<span data-ttu-id="a8206-118">Especifica a ID do agente de log específico a obter.</span><span class="sxs-lookup"><span data-stu-id="a8206-118">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by logger ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8206-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8206-119">-DefaultProfile</span></span>
<span data-ttu-id="a8206-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8206-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8206-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8206-121">CommonParameters</span></span>
<span data-ttu-id="a8206-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8206-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8206-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8206-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8206-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8206-124">INPUTS</span></span>

## <span data-ttu-id="a8206-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8206-125">OUTPUTS</span></span>

### <span data-ttu-id="a8206-126">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="a8206-126">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>

## <span data-ttu-id="a8206-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8206-127">NOTES</span></span>

## <span data-ttu-id="a8206-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8206-128">RELATED LINKS</span></span>

[<span data-ttu-id="a8206-129">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a8206-129">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="a8206-130">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a8206-130">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="a8206-131">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a8206-131">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


