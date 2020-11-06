---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431840"
---
# <span data-ttu-id="4061b-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4061b-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="4061b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4061b-102">SYNOPSIS</span></span>
<span data-ttu-id="4061b-103">Obtém todos os grupos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="4061b-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4061b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4061b-104">SYNTAX</span></span>

### <span data-ttu-id="4061b-105">Obter todos os grupos (padrão)</span><span class="sxs-lookup"><span data-stu-id="4061b-105">Get all groups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4061b-106">Obter por ID do grupo</span><span class="sxs-lookup"><span data-stu-id="4061b-106">Get by group ID</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4061b-107">Localizar grupos por usuário</span><span class="sxs-lookup"><span data-stu-id="4061b-107">Find groups by user</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4061b-108">Localizar grupos por produto</span><span class="sxs-lookup"><span data-stu-id="4061b-108">Find groups by product</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4061b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4061b-109">DESCRIPTION</span></span>
<span data-ttu-id="4061b-110">O cmdlet **Get-AzureRmApiManagementGroup** Obtém todos os grupos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="4061b-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="4061b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4061b-111">EXAMPLES</span></span>

### <span data-ttu-id="4061b-112">Exemplo 1: obter todos os grupos</span><span class="sxs-lookup"><span data-stu-id="4061b-112">Example 1: Get all groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

<span data-ttu-id="4061b-113">Esse comando obtém todos os grupos.</span><span class="sxs-lookup"><span data-stu-id="4061b-113">This command gets all groups.</span></span>

### <span data-ttu-id="4061b-114">Exemplo 2: obter um grupo por ID</span><span class="sxs-lookup"><span data-stu-id="4061b-114">Example 2: Get a group by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

<span data-ttu-id="4061b-115">Esse comando obtém a ID do grupo chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="4061b-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="4061b-116">Exemplo 3: obter um grupo por nome</span><span class="sxs-lookup"><span data-stu-id="4061b-116">Example 3: Get a group by name</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

<span data-ttu-id="4061b-117">Esse comando obtém o grupo chamado Group0002.</span><span class="sxs-lookup"><span data-stu-id="4061b-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="4061b-118">Exemplo 4: obter todos os grupos de usuários</span><span class="sxs-lookup"><span data-stu-id="4061b-118">Example 4: Get all user groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

<span data-ttu-id="4061b-119">Esse comando obtém todos os grupos de usuários com a ID de usuário chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="4061b-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="4061b-120">OS</span><span class="sxs-lookup"><span data-stu-id="4061b-120">PARAMETERS</span></span>

### <span data-ttu-id="4061b-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4061b-121">-Context</span></span>
<span data-ttu-id="4061b-122">Especifica uma instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4061b-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="4061b-123">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4061b-123">-GroupId</span></span>
<span data-ttu-id="4061b-124">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="4061b-124">Specifies the group ID.</span></span>
<span data-ttu-id="4061b-125">Se especificado, o cmdlet tenta localizar o grupo pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="4061b-125">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4061b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4061b-126">-Name</span></span>
<span data-ttu-id="4061b-127">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="4061b-127">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="4061b-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4061b-128">-ProductId</span></span>
<span data-ttu-id="4061b-129">Identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="4061b-129">Identifier of existing product.</span></span>
<span data-ttu-id="4061b-130">Se especificado, retornará todos os grupos aos quais o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="4061b-130">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="4061b-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4061b-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4061b-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="4061b-132">-UserId</span></span>
<span data-ttu-id="4061b-133">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="4061b-133">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="4061b-134">Se especificado, o cmdlet retornará todos os grupos aos quais o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="4061b-134">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4061b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4061b-135">-DefaultProfile</span></span>
<span data-ttu-id="4061b-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4061b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4061b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4061b-137">CommonParameters</span></span>
<span data-ttu-id="4061b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4061b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4061b-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4061b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4061b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4061b-140">INPUTS</span></span>

## <span data-ttu-id="4061b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4061b-141">OUTPUTS</span></span>

### <span data-ttu-id="4061b-142">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="4061b-142">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>

## <span data-ttu-id="4061b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4061b-143">NOTES</span></span>

## <span data-ttu-id="4061b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4061b-144">RELATED LINKS</span></span>

[<span data-ttu-id="4061b-145">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4061b-145">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="4061b-146">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4061b-146">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="4061b-147">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4061b-147">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


