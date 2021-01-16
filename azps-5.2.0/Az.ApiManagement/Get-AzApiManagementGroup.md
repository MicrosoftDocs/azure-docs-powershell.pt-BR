---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263398"
---
# <span data-ttu-id="76fa8-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="76fa8-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="76fa8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="76fa8-103">Obtém todos os grupos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="76fa8-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="76fa8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76fa8-104">SYNTAX</span></span>

### <span data-ttu-id="76fa8-105">GetAllGroups (padrão)</span><span class="sxs-lookup"><span data-stu-id="76fa8-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fa8-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="76fa8-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fa8-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="76fa8-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fa8-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="76fa8-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76fa8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76fa8-109">DESCRIPTION</span></span>
<span data-ttu-id="76fa8-110">O cmdlet **Get-AzApiManagementGroup** Obtém todos os grupos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="76fa8-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="76fa8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76fa8-111">EXAMPLES</span></span>

### <span data-ttu-id="76fa8-112">Exemplo 1: obter todos os grupos</span><span class="sxs-lookup"><span data-stu-id="76fa8-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="76fa8-113">Esse comando obtém todos os grupos.</span><span class="sxs-lookup"><span data-stu-id="76fa8-113">This command gets all groups.</span></span>

### <span data-ttu-id="76fa8-114">Exemplo 2: obter um grupo por ID</span><span class="sxs-lookup"><span data-stu-id="76fa8-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="76fa8-115">Esse comando obtém a ID do grupo chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="76fa8-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="76fa8-116">Exemplo 3: obter um grupo por nome</span><span class="sxs-lookup"><span data-stu-id="76fa8-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="76fa8-117">Esse comando obtém o grupo chamado Group0002.</span><span class="sxs-lookup"><span data-stu-id="76fa8-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="76fa8-118">Exemplo 4: obter todos os grupos de usuários</span><span class="sxs-lookup"><span data-stu-id="76fa8-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="76fa8-119">Esse comando obtém todos os grupos de usuários com a ID de usuário chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="76fa8-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="76fa8-120">OS</span><span class="sxs-lookup"><span data-stu-id="76fa8-120">PARAMETERS</span></span>

### <span data-ttu-id="76fa8-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="76fa8-121">-Context</span></span>
<span data-ttu-id="76fa8-122">Especifica uma instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="76fa8-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="76fa8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fa8-123">-DefaultProfile</span></span>
<span data-ttu-id="76fa8-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76fa8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76fa8-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="76fa8-125">-GroupId</span></span>
<span data-ttu-id="76fa8-126">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="76fa8-126">Specifies the group ID.</span></span>
<span data-ttu-id="76fa8-127">Se especificado, o cmdlet tenta localizar o grupo pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="76fa8-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="76fa8-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="76fa8-128">-Name</span></span>
<span data-ttu-id="76fa8-129">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="76fa8-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="76fa8-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="76fa8-130">-ProductId</span></span>
<span data-ttu-id="76fa8-131">Identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="76fa8-131">Identifier of existing product.</span></span>
<span data-ttu-id="76fa8-132">Se especificado, retornará todos os grupos aos quais o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="76fa8-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="76fa8-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76fa8-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="76fa8-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="76fa8-134">-UserId</span></span>
<span data-ttu-id="76fa8-135">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="76fa8-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="76fa8-136">Se especificado, o cmdlet retornará todos os grupos aos quais o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="76fa8-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="76fa8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fa8-137">CommonParameters</span></span>
<span data-ttu-id="76fa8-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76fa8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fa8-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76fa8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fa8-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76fa8-140">INPUTS</span></span>

### <span data-ttu-id="76fa8-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76fa8-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76fa8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="76fa8-142">System.String</span></span>

## <span data-ttu-id="76fa8-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76fa8-143">OUTPUTS</span></span>

### <span data-ttu-id="76fa8-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="76fa8-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="76fa8-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76fa8-145">NOTES</span></span>

## <span data-ttu-id="76fa8-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76fa8-146">RELATED LINKS</span></span>

[<span data-ttu-id="76fa8-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="76fa8-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="76fa8-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="76fa8-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="76fa8-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="76fa8-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


