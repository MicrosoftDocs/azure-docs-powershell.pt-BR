---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: c5bbe6413a17707e7c25a616c3c67d6b7d5da5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432824"
---
# <span data-ttu-id="66c07-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="66c07-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="66c07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66c07-102">SYNOPSIS</span></span>
<span data-ttu-id="66c07-103">Cria um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="66c07-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66c07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66c07-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66c07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66c07-105">DESCRIPTION</span></span>
<span data-ttu-id="66c07-106">O cmdlet **New-AzureRmApiManagementGroup** cria um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="66c07-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="66c07-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66c07-107">EXAMPLES</span></span>

### <span data-ttu-id="66c07-108">Exemplo 1: criar um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="66c07-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="66c07-109">Esse comando cria um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="66c07-109">This command creates a management group.</span></span>

## <span data-ttu-id="66c07-110">OS</span><span class="sxs-lookup"><span data-stu-id="66c07-110">PARAMETERS</span></span>

### <span data-ttu-id="66c07-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="66c07-111">-Context</span></span>
<span data-ttu-id="66c07-112">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="66c07-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="66c07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c07-113">-DefaultProfile</span></span>
<span data-ttu-id="66c07-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66c07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66c07-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="66c07-115">-Description</span></span>
<span data-ttu-id="66c07-116">Especifica a descrição do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="66c07-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="66c07-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="66c07-117">-ExternalId</span></span>
<span data-ttu-id="66c07-118">Para grupos externos, essa propriedade contém a ID do grupo do provedor de identidade externa, por exemplo, Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; caso contrário, o valor será nulo.</span><span class="sxs-lookup"><span data-stu-id="66c07-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c07-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="66c07-119">-GroupId</span></span>
<span data-ttu-id="66c07-120">Especifica o identificador do novo grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="66c07-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="66c07-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="66c07-121">-Name</span></span>
<span data-ttu-id="66c07-122">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="66c07-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="66c07-123">-Digite</span><span class="sxs-lookup"><span data-stu-id="66c07-123">-Type</span></span>
<span data-ttu-id="66c07-124">Tipo de grupo.</span><span class="sxs-lookup"><span data-stu-id="66c07-124">Group Type.</span></span> <span data-ttu-id="66c07-125">Grupo personalizado é o grupo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="66c07-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="66c07-126">O grupo sistema inclui administrador, desenvolvedores e convidados.</span><span class="sxs-lookup"><span data-stu-id="66c07-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="66c07-127">Não é possível criar ou atualizar um grupo do sistema.</span><span class="sxs-lookup"><span data-stu-id="66c07-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="66c07-128">Grupo externo são grupos do provedor de identidade externa, como o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="66c07-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="66c07-129">Esse parâmetro é opcional e, por padrão, assumido como um grupo personalizado.</span><span class="sxs-lookup"><span data-stu-id="66c07-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c07-130">CommonParameters</span></span>
<span data-ttu-id="66c07-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c07-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c07-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c07-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66c07-133">INPUTS</span></span>

### <span data-ttu-id="66c07-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66c07-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66c07-135">System. String</span><span class="sxs-lookup"><span data-stu-id="66c07-135">System.String</span></span>

### <span data-ttu-id="66c07-136">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementGroupType, Microsoft. Azure. Commands. ApiManagement. onmanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="66c07-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="66c07-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66c07-137">OUTPUTS</span></span>

### <span data-ttu-id="66c07-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="66c07-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="66c07-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66c07-139">NOTES</span></span>

## <span data-ttu-id="66c07-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66c07-140">RELATED LINKS</span></span>

[<span data-ttu-id="66c07-141">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="66c07-141">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="66c07-142">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="66c07-142">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="66c07-143">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="66c07-143">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


