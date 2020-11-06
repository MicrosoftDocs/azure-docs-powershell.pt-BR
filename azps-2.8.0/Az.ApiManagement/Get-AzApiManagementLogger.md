---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: 219c78dbcd39a922f98a185deb1e6ce6f0c3b652
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598107"
---
# <span data-ttu-id="fdea3-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fdea3-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="fdea3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdea3-102">SYNOPSIS</span></span>
<span data-ttu-id="fdea3-103">Obtém objetos de agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="fdea3-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="fdea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdea3-104">SYNTAX</span></span>

### <span data-ttu-id="fdea3-105">GetAllLoggers (padrão)</span><span class="sxs-lookup"><span data-stu-id="fdea3-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdea3-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="fdea3-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdea3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdea3-107">DESCRIPTION</span></span>
<span data-ttu-id="fdea3-108">O cmdlet **Get-AzApiManagementLogger** Obtém um **agente** de gerenciamento de API do Azure ou todos os registradores.</span><span class="sxs-lookup"><span data-stu-id="fdea3-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="fdea3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdea3-109">EXAMPLES</span></span>

### <span data-ttu-id="fdea3-110">Exemplo 1: obter todos os registradores</span><span class="sxs-lookup"><span data-stu-id="fdea3-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="fdea3-111">Esse comando obtém todos os loggers do contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="fdea3-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="fdea3-112">Exemplo 2: obter um agente de log específico</span><span class="sxs-lookup"><span data-stu-id="fdea3-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="fdea3-113">Esse comando Remove um logger que tem a ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="fdea3-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="fdea3-114">OS</span><span class="sxs-lookup"><span data-stu-id="fdea3-114">PARAMETERS</span></span>

### <span data-ttu-id="fdea3-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fdea3-115">-Context</span></span>
<span data-ttu-id="fdea3-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fdea3-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fdea3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdea3-117">-DefaultProfile</span></span>
<span data-ttu-id="fdea3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdea3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdea3-119">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="fdea3-119">-LoggerId</span></span>
<span data-ttu-id="fdea3-120">Especifica a ID do agente de log específico a obter.</span><span class="sxs-lookup"><span data-stu-id="fdea3-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdea3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdea3-121">CommonParameters</span></span>
<span data-ttu-id="fdea3-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdea3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdea3-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdea3-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdea3-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdea3-124">INPUTS</span></span>

### <span data-ttu-id="fdea3-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fdea3-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fdea3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fdea3-126">System.String</span></span>

## <span data-ttu-id="fdea3-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdea3-127">OUTPUTS</span></span>

### <span data-ttu-id="fdea3-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fdea3-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="fdea3-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdea3-129">NOTES</span></span>

## <span data-ttu-id="fdea3-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdea3-130">RELATED LINKS</span></span>

[<span data-ttu-id="fdea3-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fdea3-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="fdea3-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fdea3-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="fdea3-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fdea3-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


