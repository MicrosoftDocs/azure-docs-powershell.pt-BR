---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118065"
---
# <span data-ttu-id="91736-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="91736-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="91736-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91736-102">SYNOPSIS</span></span>
<span data-ttu-id="91736-103">Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="91736-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="91736-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91736-104">SYNTAX</span></span>

### <span data-ttu-id="91736-105">GetAllApiOperations (Padrão)</span><span class="sxs-lookup"><span data-stu-id="91736-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91736-106">GetById</span><span class="sxs-lookup"><span data-stu-id="91736-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91736-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="91736-107">DESCRIPTION</span></span>
<span data-ttu-id="91736-108">O **Get-AzApiManagementOperation** obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="91736-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="91736-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91736-109">EXAMPLES</span></span>

### <span data-ttu-id="91736-110">Exemplo 1: Obter todas as operações de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="91736-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="91736-111">Esse comando obtém todas as operações de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="91736-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="91736-112">Exemplo 2: Obter uma operação de Gerenciamento de API por ID de operação</span><span class="sxs-lookup"><span data-stu-id="91736-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="91736-113">Esse comando obtém uma operação de gerenciamento de API pela ID da operação chamada Operation0003.</span><span class="sxs-lookup"><span data-stu-id="91736-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="91736-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91736-114">PARAMETERS</span></span>

### <span data-ttu-id="91736-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="91736-115">-ApiId</span></span>
<span data-ttu-id="91736-116">Especifica o identificador da Operação da API.</span><span class="sxs-lookup"><span data-stu-id="91736-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="91736-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="91736-117">-ApiRevision</span></span>
<span data-ttu-id="91736-118">Identificador de Revisão da API.</span><span class="sxs-lookup"><span data-stu-id="91736-118">Identifier of API Revision.</span></span> <span data-ttu-id="91736-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="91736-119">This parameter is optional.</span></span> <span data-ttu-id="91736-120">Se não especificado, a operação será recuperada da revisão da api ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="91736-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="91736-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="91736-121">-Context</span></span>
<span data-ttu-id="91736-122">Especifica a instância do objeto **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="91736-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91736-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91736-123">-DefaultProfile</span></span>
<span data-ttu-id="91736-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="91736-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91736-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="91736-125">-OperationId</span></span>
<span data-ttu-id="91736-126">Especifica o identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="91736-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91736-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91736-127">CommonParameters</span></span>
<span data-ttu-id="91736-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91736-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91736-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91736-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91736-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="91736-130">INPUTS</span></span>

### <span data-ttu-id="91736-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="91736-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91736-132">System.String</span><span class="sxs-lookup"><span data-stu-id="91736-132">System.String</span></span>

## <span data-ttu-id="91736-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="91736-133">OUTPUTS</span></span>

### <span data-ttu-id="91736-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="91736-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="91736-135">Notas</span><span class="sxs-lookup"><span data-stu-id="91736-135">NOTES</span></span>

## <span data-ttu-id="91736-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91736-136">RELATED LINKS</span></span>

[<span data-ttu-id="91736-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="91736-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="91736-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="91736-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="91736-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="91736-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


