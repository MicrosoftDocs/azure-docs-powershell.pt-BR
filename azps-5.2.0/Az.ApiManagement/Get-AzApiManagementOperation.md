---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260942"
---
# <span data-ttu-id="a729b-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a729b-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="a729b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a729b-102">SYNOPSIS</span></span>
<span data-ttu-id="a729b-103">Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="a729b-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="a729b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a729b-104">SYNTAX</span></span>

### <span data-ttu-id="a729b-105">GetAllApiOperations (padrão)</span><span class="sxs-lookup"><span data-stu-id="a729b-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a729b-106">GetById</span><span class="sxs-lookup"><span data-stu-id="a729b-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a729b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a729b-107">DESCRIPTION</span></span>
<span data-ttu-id="a729b-108">**Get-AzApiManagementOperation** Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="a729b-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="a729b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a729b-109">EXAMPLES</span></span>

### <span data-ttu-id="a729b-110">Exemplo 1: obter todas as operações de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="a729b-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="a729b-111">Esse comando obtém todas as operações de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a729b-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="a729b-112">Exemplo 2: obter uma operação de gerenciamento de API por ID da operação</span><span class="sxs-lookup"><span data-stu-id="a729b-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="a729b-113">Esse comando obtém uma operação de gerenciamento de API por ID de operação chamada Operation0003.</span><span class="sxs-lookup"><span data-stu-id="a729b-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="a729b-114">OS</span><span class="sxs-lookup"><span data-stu-id="a729b-114">PARAMETERS</span></span>

### <span data-ttu-id="a729b-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a729b-115">-ApiId</span></span>
<span data-ttu-id="a729b-116">Especifica o identificador da operação de API.</span><span class="sxs-lookup"><span data-stu-id="a729b-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="a729b-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a729b-117">-ApiRevision</span></span>
<span data-ttu-id="a729b-118">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="a729b-118">Identifier of API Revision.</span></span> <span data-ttu-id="a729b-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a729b-119">This parameter is optional.</span></span> <span data-ttu-id="a729b-120">Se não for especificado, a operação será recuperada da revisão da API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="a729b-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="a729b-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a729b-121">-Context</span></span>
<span data-ttu-id="a729b-122">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a729b-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a729b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a729b-123">-DefaultProfile</span></span>
<span data-ttu-id="a729b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a729b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a729b-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a729b-125">-OperationId</span></span>
<span data-ttu-id="a729b-126">Especifica o identificador da operação.</span><span class="sxs-lookup"><span data-stu-id="a729b-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="a729b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a729b-127">CommonParameters</span></span>
<span data-ttu-id="a729b-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a729b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a729b-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a729b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a729b-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a729b-130">INPUTS</span></span>

### <span data-ttu-id="a729b-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a729b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a729b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a729b-132">System.String</span></span>

## <span data-ttu-id="a729b-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a729b-133">OUTPUTS</span></span>

### <span data-ttu-id="a729b-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a729b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="a729b-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a729b-135">NOTES</span></span>

## <span data-ttu-id="a729b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a729b-136">RELATED LINKS</span></span>

[<span data-ttu-id="a729b-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a729b-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="a729b-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a729b-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="a729b-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a729b-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


