---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: aafe70a476dbf983e8ae68b0f1fadf021b2990f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888012"
---
# <span data-ttu-id="b31ce-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b31ce-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="b31ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b31ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b31ce-103">Obtém objetos do Api Management Logger.</span><span class="sxs-lookup"><span data-stu-id="b31ce-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="b31ce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b31ce-104">SYNTAX</span></span>

### <span data-ttu-id="b31ce-105">GetAllLoggers (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b31ce-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b31ce-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="b31ce-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b31ce-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b31ce-107">DESCRIPTION</span></span>
<span data-ttu-id="b31ce-108">O cmdlet **Get-AzApiManagementLogger** obtém um Azure API Management **Logger** ou todos os madeireiros.</span><span class="sxs-lookup"><span data-stu-id="b31ce-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="b31ce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b31ce-109">EXAMPLES</span></span>

### <span data-ttu-id="b31ce-110">Exemplo 1: Obter todos os madeireiros</span><span class="sxs-lookup"><span data-stu-id="b31ce-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="b31ce-111">Esse comando obtém todos os madeireiros para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="b31ce-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="b31ce-112">Exemplo 2: Obter um madeireiro específico</span><span class="sxs-lookup"><span data-stu-id="b31ce-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="b31ce-113">Este comando remove um madeireiro que tem o ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="b31ce-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="b31ce-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b31ce-114">PARAMETERS</span></span>

### <span data-ttu-id="b31ce-115">-Context</span><span class="sxs-lookup"><span data-stu-id="b31ce-115">-Context</span></span>
<span data-ttu-id="b31ce-116">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="b31ce-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b31ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31ce-117">-DefaultProfile</span></span>
<span data-ttu-id="b31ce-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b31ce-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b31ce-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="b31ce-119">-LoggerId</span></span>
<span data-ttu-id="b31ce-120">Especifica a ID do madeireiro específico a ser obter.</span><span class="sxs-lookup"><span data-stu-id="b31ce-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="b31ce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31ce-121">CommonParameters</span></span>
<span data-ttu-id="b31ce-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b31ce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31ce-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b31ce-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31ce-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b31ce-124">INPUTS</span></span>

### <span data-ttu-id="b31ce-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b31ce-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b31ce-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b31ce-126">System.String</span></span>

## <span data-ttu-id="b31ce-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b31ce-127">OUTPUTS</span></span>

### <span data-ttu-id="b31ce-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b31ce-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="b31ce-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="b31ce-129">NOTES</span></span>

## <span data-ttu-id="b31ce-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b31ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="b31ce-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b31ce-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="b31ce-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b31ce-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="b31ce-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b31ce-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


