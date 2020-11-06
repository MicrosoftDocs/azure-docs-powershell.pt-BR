---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: b77452bff93a9b66f8ffe54fdff623d391749622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432516"
---
# <span data-ttu-id="5266e-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5266e-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="5266e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5266e-102">SYNOPSIS</span></span>
<span data-ttu-id="5266e-103">Obtém todos os grupos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="5266e-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5266e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5266e-104">SYNTAX</span></span>

### <span data-ttu-id="5266e-105">GetAllGroups (padrão)</span><span class="sxs-lookup"><span data-stu-id="5266e-105">GetAllGroups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5266e-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="5266e-106">GetByGroupId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5266e-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="5266e-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5266e-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="5266e-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5266e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5266e-109">DESCRIPTION</span></span>
<span data-ttu-id="5266e-110">O cmdlet **Get-AzureRmApiManagementGroup** Obtém todos os grupos ou grupos de gerenciamento de API específicos.</span><span class="sxs-lookup"><span data-stu-id="5266e-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="5266e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5266e-111">EXAMPLES</span></span>

### <span data-ttu-id="5266e-112">Exemplo 1: obter todos os grupos</span><span class="sxs-lookup"><span data-stu-id="5266e-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

<span data-ttu-id="5266e-113">Esse comando obtém todos os grupos.</span><span class="sxs-lookup"><span data-stu-id="5266e-113">This command gets all groups.</span></span>

### <span data-ttu-id="5266e-114">Exemplo 2: obter um grupo por ID</span><span class="sxs-lookup"><span data-stu-id="5266e-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="5266e-115">Esse comando obtém a ID do grupo chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="5266e-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="5266e-116">Exemplo 3: obter um grupo por nome</span><span class="sxs-lookup"><span data-stu-id="5266e-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="5266e-117">Esse comando obtém o grupo chamado Group0002.</span><span class="sxs-lookup"><span data-stu-id="5266e-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="5266e-118">Exemplo 4: obter todos os grupos de usuários</span><span class="sxs-lookup"><span data-stu-id="5266e-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="5266e-119">Esse comando obtém todos os grupos de usuários com a ID de usuário chamada 0123456789.</span><span class="sxs-lookup"><span data-stu-id="5266e-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="5266e-120">OS</span><span class="sxs-lookup"><span data-stu-id="5266e-120">PARAMETERS</span></span>

### <span data-ttu-id="5266e-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5266e-121">-Context</span></span>
<span data-ttu-id="5266e-122">Especifica uma instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5266e-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5266e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5266e-123">-DefaultProfile</span></span>
<span data-ttu-id="5266e-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5266e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5266e-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="5266e-125">-GroupId</span></span>
<span data-ttu-id="5266e-126">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="5266e-126">Specifies the group ID.</span></span>
<span data-ttu-id="5266e-127">Se especificado, o cmdlet tenta localizar o grupo pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="5266e-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByGroupId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5266e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="5266e-128">-Name</span></span>
<span data-ttu-id="5266e-129">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="5266e-129">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5266e-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5266e-130">-ProductId</span></span>
<span data-ttu-id="5266e-131">Identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="5266e-131">Identifier of existing product.</span></span>
<span data-ttu-id="5266e-132">Se especificado, retornará todos os grupos aos quais o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="5266e-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="5266e-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5266e-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5266e-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="5266e-134">-UserId</span></span>
<span data-ttu-id="5266e-135">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="5266e-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="5266e-136">Se especificado, o cmdlet retornará todos os grupos aos quais o produto atribuído.</span><span class="sxs-lookup"><span data-stu-id="5266e-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5266e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5266e-137">CommonParameters</span></span>
<span data-ttu-id="5266e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5266e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5266e-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5266e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5266e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5266e-140">INPUTS</span></span>

### <span data-ttu-id="5266e-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5266e-141">None</span></span>
<span data-ttu-id="5266e-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5266e-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5266e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5266e-143">OUTPUTS</span></span>

### <span data-ttu-id="5266e-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5266e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>
<span data-ttu-id="5266e-145">Os detalhes do grupo configurado no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5266e-145">The details of the Group configured in API Management service.</span></span>

### <span data-ttu-id="5266e-146">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="5266e-146">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>
<span data-ttu-id="5266e-147">A lista de grupos configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5266e-147">The list of Groups configured in API Management service.</span></span>

## <span data-ttu-id="5266e-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5266e-148">NOTES</span></span>

## <span data-ttu-id="5266e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5266e-149">RELATED LINKS</span></span>

[<span data-ttu-id="5266e-150">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5266e-150">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="5266e-151">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5266e-151">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="5266e-152">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5266e-152">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


