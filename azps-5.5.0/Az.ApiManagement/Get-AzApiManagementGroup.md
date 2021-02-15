---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118075"
---
# <span data-ttu-id="5f55f-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f55f-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="5f55f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f55f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f55f-103">Obtém grupos de gerenciamento de API específicos ou todos.</span><span class="sxs-lookup"><span data-stu-id="5f55f-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="5f55f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f55f-104">SYNTAX</span></span>

### <span data-ttu-id="5f55f-105">GetAllGroups (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5f55f-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f55f-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="5f55f-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f55f-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="5f55f-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f55f-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="5f55f-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f55f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f55f-109">DESCRIPTION</span></span>
<span data-ttu-id="5f55f-110">O cmdlet **Get-AzApiManagementGroup** obtém grupos de gerenciamento de API específicos ou todos.</span><span class="sxs-lookup"><span data-stu-id="5f55f-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="5f55f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5f55f-111">EXAMPLES</span></span>

### <span data-ttu-id="5f55f-112">Exemplo 1: Obter todos os grupos</span><span class="sxs-lookup"><span data-stu-id="5f55f-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="5f55f-113">Esse comando obtém todos os grupos.</span><span class="sxs-lookup"><span data-stu-id="5f55f-113">This command gets all groups.</span></span>

### <span data-ttu-id="5f55f-114">Exemplo 2: Obter um grupo por ID</span><span class="sxs-lookup"><span data-stu-id="5f55f-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="5f55f-115">Esse comando obtém a ID do grupo chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="5f55f-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="5f55f-116">Exemplo 3: Obter um grupo por nome</span><span class="sxs-lookup"><span data-stu-id="5f55f-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="5f55f-117">Esse comando obtém o grupo chamado Group0002.</span><span class="sxs-lookup"><span data-stu-id="5f55f-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="5f55f-118">Exemplo 4: Obter todos os grupos de usuários</span><span class="sxs-lookup"><span data-stu-id="5f55f-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="5f55f-119">Esse comando obtém todos os grupos de usuários com a ID de usuário chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="5f55f-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="5f55f-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f55f-120">PARAMETERS</span></span>

### <span data-ttu-id="5f55f-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5f55f-121">-Context</span></span>
<span data-ttu-id="5f55f-122">Especifica uma instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5f55f-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="5f55f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f55f-123">-DefaultProfile</span></span>
<span data-ttu-id="5f55f-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5f55f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f55f-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="5f55f-125">-GroupId</span></span>
<span data-ttu-id="5f55f-126">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="5f55f-126">Specifies the group ID.</span></span>
<span data-ttu-id="5f55f-127">Se especificado, o cmdlet tentará encontrar o grupo pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="5f55f-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="5f55f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f55f-128">-Name</span></span>
<span data-ttu-id="5f55f-129">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="5f55f-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="5f55f-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5f55f-130">-ProductId</span></span>
<span data-ttu-id="5f55f-131">Identificador de produto existente.</span><span class="sxs-lookup"><span data-stu-id="5f55f-131">Identifier of existing product.</span></span>
<span data-ttu-id="5f55f-132">Se especificado, retornará todos os grupos aos que o produto foi atribuído.</span><span class="sxs-lookup"><span data-stu-id="5f55f-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="5f55f-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5f55f-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f55f-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="5f55f-134">-UserId</span></span>
<span data-ttu-id="5f55f-135">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="5f55f-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="5f55f-136">Se especificado, o cmdlet retornará todos os grupos aos produtos atribuídos.</span><span class="sxs-lookup"><span data-stu-id="5f55f-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="5f55f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f55f-137">CommonParameters</span></span>
<span data-ttu-id="5f55f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f55f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f55f-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f55f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f55f-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="5f55f-140">INPUTS</span></span>

### <span data-ttu-id="5f55f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5f55f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5f55f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5f55f-142">System.String</span></span>

## <span data-ttu-id="5f55f-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="5f55f-143">OUTPUTS</span></span>

### <span data-ttu-id="5f55f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f55f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="5f55f-145">Notas</span><span class="sxs-lookup"><span data-stu-id="5f55f-145">NOTES</span></span>

## <span data-ttu-id="5f55f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f55f-146">RELATED LINKS</span></span>

[<span data-ttu-id="5f55f-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f55f-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="5f55f-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f55f-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="5f55f-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f55f-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


