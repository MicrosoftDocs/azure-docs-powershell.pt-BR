---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 5807925c302f951f9e48c89afcb62634bd774c89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901370"
---
# <span data-ttu-id="104b0-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="104b0-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="104b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="104b0-102">SYNOPSIS</span></span>
<span data-ttu-id="104b0-103">Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="104b0-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="104b0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="104b0-104">SYNTAX</span></span>

### <span data-ttu-id="104b0-105">GetAllApiOperations (Padrão)</span><span class="sxs-lookup"><span data-stu-id="104b0-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="104b0-106">GetById</span><span class="sxs-lookup"><span data-stu-id="104b0-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="104b0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="104b0-107">DESCRIPTION</span></span>
<span data-ttu-id="104b0-108">**Get-AzApiManagementOperation** obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="104b0-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="104b0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="104b0-109">EXAMPLES</span></span>

### <span data-ttu-id="104b0-110">Exemplo 1: Obter todas as operações de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="104b0-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="104b0-111">Este comando obtém todas as operações de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="104b0-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="104b0-112">Exemplo 2: Obter uma operação de Gerenciamento de API por ID de operação</span><span class="sxs-lookup"><span data-stu-id="104b0-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="104b0-113">Este comando obtém uma operação de gerenciamento de API por ID da operação chamada Operation0003.</span><span class="sxs-lookup"><span data-stu-id="104b0-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="104b0-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="104b0-114">PARAMETERS</span></span>

### <span data-ttu-id="104b0-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="104b0-115">-ApiId</span></span>
<span data-ttu-id="104b0-116">Especifica o identificador da Operação da API.</span><span class="sxs-lookup"><span data-stu-id="104b0-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="104b0-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="104b0-117">-ApiRevision</span></span>
<span data-ttu-id="104b0-118">Identificador da Revisão da API.</span><span class="sxs-lookup"><span data-stu-id="104b0-118">Identifier of API Revision.</span></span> <span data-ttu-id="104b0-119">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="104b0-119">This parameter is optional.</span></span> <span data-ttu-id="104b0-120">Se não for especificada, a operação será recuperada da revisão da api ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="104b0-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="104b0-121">-Context</span><span class="sxs-lookup"><span data-stu-id="104b0-121">-Context</span></span>
<span data-ttu-id="104b0-122">Especifica a instância do **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="104b0-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="104b0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="104b0-123">-DefaultProfile</span></span>
<span data-ttu-id="104b0-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="104b0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="104b0-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="104b0-125">-OperationId</span></span>
<span data-ttu-id="104b0-126">Especifica o identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="104b0-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="104b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="104b0-127">CommonParameters</span></span>
<span data-ttu-id="104b0-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="104b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="104b0-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="104b0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="104b0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="104b0-130">INPUTS</span></span>

### <span data-ttu-id="104b0-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="104b0-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="104b0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="104b0-132">System.String</span></span>

## <span data-ttu-id="104b0-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="104b0-133">OUTPUTS</span></span>

### <span data-ttu-id="104b0-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="104b0-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="104b0-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="104b0-135">NOTES</span></span>

## <span data-ttu-id="104b0-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="104b0-136">RELATED LINKS</span></span>

[<span data-ttu-id="104b0-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="104b0-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="104b0-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="104b0-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="104b0-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="104b0-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


