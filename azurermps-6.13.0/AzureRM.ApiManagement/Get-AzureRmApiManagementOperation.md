---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 469d10303f286a0feca162e628a1564826b850d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426518"
---
# <span data-ttu-id="d0443-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d0443-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="d0443-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0443-102">SYNOPSIS</span></span>
<span data-ttu-id="d0443-103">Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="d0443-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0443-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0443-104">SYNTAX</span></span>

### <span data-ttu-id="d0443-105">GetAllApiOperations (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0443-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0443-106">GetById</span><span class="sxs-lookup"><span data-stu-id="d0443-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0443-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0443-107">DESCRIPTION</span></span>
<span data-ttu-id="d0443-108">**Get-AzureRmApiManagementOperation** Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="d0443-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="d0443-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0443-109">EXAMPLES</span></span>

### <span data-ttu-id="d0443-110">Exemplo 1: obter todas as operações de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="d0443-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="d0443-111">Esse comando obtém todas as operações de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="d0443-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="d0443-112">Exemplo 2: obter uma operação de gerenciamento de API por ID da operação</span><span class="sxs-lookup"><span data-stu-id="d0443-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="d0443-113">Esse comando obtém uma operação de gerenciamento de API por ID de operação chamada Operation0003.</span><span class="sxs-lookup"><span data-stu-id="d0443-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="d0443-114">OS</span><span class="sxs-lookup"><span data-stu-id="d0443-114">PARAMETERS</span></span>

### <span data-ttu-id="d0443-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d0443-115">-ApiId</span></span>
<span data-ttu-id="d0443-116">Especifica o identificador da operação de API.</span><span class="sxs-lookup"><span data-stu-id="d0443-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="d0443-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d0443-117">-ApiRevision</span></span>
<span data-ttu-id="d0443-118">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="d0443-118">Identifier of API Revision.</span></span> <span data-ttu-id="d0443-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d0443-119">This parameter is optional.</span></span> <span data-ttu-id="d0443-120">Se não for especificado, a operação será recuperada da revisão da API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="d0443-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="d0443-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d0443-121">-Context</span></span>
<span data-ttu-id="d0443-122">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d0443-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d0443-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0443-123">-DefaultProfile</span></span>
<span data-ttu-id="d0443-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0443-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0443-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d0443-125">-OperationId</span></span>
<span data-ttu-id="d0443-126">Especifica o identificador da operação.</span><span class="sxs-lookup"><span data-stu-id="d0443-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="d0443-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0443-127">CommonParameters</span></span>
<span data-ttu-id="d0443-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0443-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0443-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0443-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0443-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0443-130">INPUTS</span></span>

### <span data-ttu-id="d0443-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d0443-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d0443-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d0443-132">System.String</span></span>

## <span data-ttu-id="d0443-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0443-133">OUTPUTS</span></span>

### <span data-ttu-id="d0443-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d0443-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="d0443-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0443-135">NOTES</span></span>

## <span data-ttu-id="d0443-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0443-136">RELATED LINKS</span></span>

[<span data-ttu-id="d0443-137">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d0443-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d0443-138">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d0443-138">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d0443-139">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d0443-139">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


