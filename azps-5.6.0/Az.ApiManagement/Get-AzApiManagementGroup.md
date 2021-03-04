---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: 786d095b7750843688b4319eec7e46263332a4c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886502"
---
# <span data-ttu-id="cbcb5-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cbcb5-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="cbcb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbcb5-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcb5-103">Obtém todos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="cbcb5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cbcb5-104">SYNTAX</span></span>

### <span data-ttu-id="cbcb5-105">GetAllGroups (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cbcb5-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbcb5-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="cbcb5-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbcb5-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="cbcb5-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbcb5-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="cbcb5-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbcb5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cbcb5-109">DESCRIPTION</span></span>
<span data-ttu-id="cbcb5-110">O cmdlet **Get-AzApiManagementGroup** obtém todos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="cbcb5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbcb5-111">EXAMPLES</span></span>

### <span data-ttu-id="cbcb5-112">Exemplo 1: Obter todos os grupos</span><span class="sxs-lookup"><span data-stu-id="cbcb5-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="cbcb5-113">Este comando obtém todos os grupos.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-113">This command gets all groups.</span></span>

### <span data-ttu-id="cbcb5-114">Exemplo 2: Obter um grupo por ID</span><span class="sxs-lookup"><span data-stu-id="cbcb5-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="cbcb5-115">Este comando obtém a ID do grupo chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="cbcb5-116">Exemplo 3: Obter um grupo pelo nome</span><span class="sxs-lookup"><span data-stu-id="cbcb5-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="cbcb5-117">Este comando obtém o grupo chamado Group0002.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="cbcb5-118">Exemplo 4: Obter todos os grupos de usuários</span><span class="sxs-lookup"><span data-stu-id="cbcb5-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="cbcb5-119">Este comando obtém todos os grupos de usuários com a ID do usuário chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="cbcb5-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cbcb5-120">PARAMETERS</span></span>

### <span data-ttu-id="cbcb5-121">-Context</span><span class="sxs-lookup"><span data-stu-id="cbcb5-121">-Context</span></span>
<span data-ttu-id="cbcb5-122">Especifica uma instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="cbcb5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcb5-123">-DefaultProfile</span></span>
<span data-ttu-id="cbcb5-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbcb5-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="cbcb5-125">-GroupId</span></span>
<span data-ttu-id="cbcb5-126">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-126">Specifies the group ID.</span></span>
<span data-ttu-id="cbcb5-127">Se especificado, o cmdlet tenta encontrar o grupo pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="cbcb5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="cbcb5-128">-Name</span></span>
<span data-ttu-id="cbcb5-129">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="cbcb5-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cbcb5-130">-ProductId</span></span>
<span data-ttu-id="cbcb5-131">Identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-131">Identifier of existing product.</span></span>
<span data-ttu-id="cbcb5-132">Se especificado, retornará todos os grupos aos que o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="cbcb5-133">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="cbcb5-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="cbcb5-134">-UserId</span></span>
<span data-ttu-id="cbcb5-135">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="cbcb5-136">Se especificado, o cmdlet retornará todos os grupos aos que o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="cbcb5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcb5-137">CommonParameters</span></span>
<span data-ttu-id="cbcb5-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbcb5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcb5-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbcb5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcb5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbcb5-140">INPUTS</span></span>

### <span data-ttu-id="cbcb5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cbcb5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cbcb5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cbcb5-142">System.String</span></span>

## <span data-ttu-id="cbcb5-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cbcb5-143">OUTPUTS</span></span>

### <span data-ttu-id="cbcb5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cbcb5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="cbcb5-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="cbcb5-145">NOTES</span></span>

## <span data-ttu-id="cbcb5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbcb5-146">RELATED LINKS</span></span>

[<span data-ttu-id="cbcb5-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cbcb5-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="cbcb5-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cbcb5-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="cbcb5-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cbcb5-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


