---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: 9a8acd17f953e90cd5b4311854830da03dc4df0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598113"
---
# <span data-ttu-id="457f1-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="457f1-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="457f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="457f1-102">SYNOPSIS</span></span>
<span data-ttu-id="457f1-103">Obtém todos os grupos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="457f1-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="457f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="457f1-104">SYNTAX</span></span>

### <span data-ttu-id="457f1-105">GetAllGroups (padrão)</span><span class="sxs-lookup"><span data-stu-id="457f1-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="457f1-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="457f1-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="457f1-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="457f1-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="457f1-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="457f1-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="457f1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="457f1-109">DESCRIPTION</span></span>
<span data-ttu-id="457f1-110">O cmdlet **Get-AzApiManagementGroup** Obtém todos os grupos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="457f1-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="457f1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="457f1-111">EXAMPLES</span></span>

### <span data-ttu-id="457f1-112">Exemplo 1: obter todos os grupos</span><span class="sxs-lookup"><span data-stu-id="457f1-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="457f1-113">Esse comando obtém todos os grupos.</span><span class="sxs-lookup"><span data-stu-id="457f1-113">This command gets all groups.</span></span>

### <span data-ttu-id="457f1-114">Exemplo 2: obter um grupo por ID</span><span class="sxs-lookup"><span data-stu-id="457f1-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="457f1-115">Esse comando obtém a ID do grupo chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="457f1-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="457f1-116">Exemplo 3: obter um grupo por nome</span><span class="sxs-lookup"><span data-stu-id="457f1-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="457f1-117">Esse comando obtém o grupo chamado Group0002.</span><span class="sxs-lookup"><span data-stu-id="457f1-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="457f1-118">Exemplo 4: obter todos os grupos de usuários</span><span class="sxs-lookup"><span data-stu-id="457f1-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="457f1-119">Esse comando obtém todos os grupos de usuários com a ID de usuário chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="457f1-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="457f1-120">OS</span><span class="sxs-lookup"><span data-stu-id="457f1-120">PARAMETERS</span></span>

### <span data-ttu-id="457f1-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="457f1-121">-Context</span></span>
<span data-ttu-id="457f1-122">Especifica uma instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="457f1-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="457f1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="457f1-123">-DefaultProfile</span></span>
<span data-ttu-id="457f1-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="457f1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="457f1-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="457f1-125">-GroupId</span></span>
<span data-ttu-id="457f1-126">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="457f1-126">Specifies the group ID.</span></span>
<span data-ttu-id="457f1-127">Se especificado, o cmdlet tenta localizar o grupo pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="457f1-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="457f1-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="457f1-128">-Name</span></span>
<span data-ttu-id="457f1-129">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="457f1-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="457f1-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="457f1-130">-ProductId</span></span>
<span data-ttu-id="457f1-131">Identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="457f1-131">Identifier of existing product.</span></span>
<span data-ttu-id="457f1-132">Se especificado, retornará todos os grupos aos quais o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="457f1-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="457f1-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="457f1-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="457f1-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="457f1-134">-UserId</span></span>
<span data-ttu-id="457f1-135">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="457f1-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="457f1-136">Se especificado, o cmdlet retornará todos os grupos aos quais o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="457f1-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="457f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="457f1-137">CommonParameters</span></span>
<span data-ttu-id="457f1-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="457f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="457f1-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="457f1-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="457f1-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="457f1-140">INPUTS</span></span>

### <span data-ttu-id="457f1-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="457f1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="457f1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="457f1-142">System.String</span></span>

## <span data-ttu-id="457f1-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="457f1-143">OUTPUTS</span></span>

### <span data-ttu-id="457f1-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="457f1-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="457f1-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="457f1-145">NOTES</span></span>

## <span data-ttu-id="457f1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="457f1-146">RELATED LINKS</span></span>

[<span data-ttu-id="457f1-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="457f1-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="457f1-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="457f1-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="457f1-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="457f1-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


