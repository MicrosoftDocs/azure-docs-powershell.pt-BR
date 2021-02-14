---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110845"
---
# <span data-ttu-id="a4775-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a4775-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="a4775-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4775-102">SYNOPSIS</span></span>
<span data-ttu-id="a4775-103">Obtém objetos lo também.</span><span class="sxs-lookup"><span data-stu-id="a4775-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="a4775-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4775-104">SYNTAX</span></span>

### <span data-ttu-id="a4775-105">GetAllLoggers (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a4775-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4775-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="a4775-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4775-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4775-107">DESCRIPTION</span></span>
<span data-ttu-id="a4775-108">O cmdlet **Get-AzApiManagementLogger** obtém uma **Loção** de Gerenciamento de API do Azure ou todos os loção.</span><span class="sxs-lookup"><span data-stu-id="a4775-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="a4775-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4775-109">EXAMPLES</span></span>

### <span data-ttu-id="a4775-110">Exemplo 1: Obter todos os lagos</span><span class="sxs-lookup"><span data-stu-id="a4775-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="a4775-111">Esse comando obtém todas as loções para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="a4775-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="a4775-112">Exemplo 2: Obter um loção específico</span><span class="sxs-lookup"><span data-stu-id="a4775-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="a4775-113">Esse comando remove um lago que tem a ID Loção123.</span><span class="sxs-lookup"><span data-stu-id="a4775-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="a4775-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4775-114">PARAMETERS</span></span>

### <span data-ttu-id="a4775-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a4775-115">-Context</span></span>
<span data-ttu-id="a4775-116">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="a4775-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a4775-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4775-117">-DefaultProfile</span></span>
<span data-ttu-id="a4775-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a4775-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4775-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="a4775-119">-LoggerId</span></span>
<span data-ttu-id="a4775-120">Especifica a ID do loção específico a ser obter.</span><span class="sxs-lookup"><span data-stu-id="a4775-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="a4775-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4775-121">CommonParameters</span></span>
<span data-ttu-id="a4775-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4775-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4775-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4775-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4775-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="a4775-124">INPUTS</span></span>

### <span data-ttu-id="a4775-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a4775-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a4775-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a4775-126">System.String</span></span>

## <span data-ttu-id="a4775-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="a4775-127">OUTPUTS</span></span>

### <span data-ttu-id="a4775-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a4775-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="a4775-129">Notas</span><span class="sxs-lookup"><span data-stu-id="a4775-129">NOTES</span></span>

## <span data-ttu-id="a4775-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4775-130">RELATED LINKS</span></span>

[<span data-ttu-id="a4775-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a4775-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="a4775-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a4775-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="a4775-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a4775-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


