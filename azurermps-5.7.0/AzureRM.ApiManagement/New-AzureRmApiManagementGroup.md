---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0443b9bc3ed2666600f2d119eca5b7173b21e89d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610140"
---
# <span data-ttu-id="496a9-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="496a9-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="496a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="496a9-102">SYNOPSIS</span></span>
<span data-ttu-id="496a9-103">Cria um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="496a9-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="496a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="496a9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="496a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="496a9-105">DESCRIPTION</span></span>
<span data-ttu-id="496a9-106">O cmdlet **New-AzureRmApiManagementGroup** cria um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="496a9-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="496a9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="496a9-107">EXAMPLES</span></span>

### <span data-ttu-id="496a9-108">Exemplo 1: criar um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="496a9-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="496a9-109">Esse comando cria um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="496a9-109">This command creates a management group.</span></span>

## <span data-ttu-id="496a9-110">OS</span><span class="sxs-lookup"><span data-stu-id="496a9-110">PARAMETERS</span></span>

### <span data-ttu-id="496a9-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="496a9-111">-Context</span></span>
<span data-ttu-id="496a9-112">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="496a9-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="496a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496a9-113">-DefaultProfile</span></span>
<span data-ttu-id="496a9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="496a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="496a9-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="496a9-115">-Description</span></span>
<span data-ttu-id="496a9-116">Especifica a descrição do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="496a9-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="496a9-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="496a9-117">-ExternalId</span></span>
<span data-ttu-id="496a9-118">Para grupos externos, essa propriedade contém a ID do grupo do provedor de identidade externa, por exemplo, Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; caso contrário, o valor será nulo.</span><span class="sxs-lookup"><span data-stu-id="496a9-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496a9-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="496a9-119">-GroupId</span></span>
<span data-ttu-id="496a9-120">Especifica o identificador do novo grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="496a9-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="496a9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="496a9-121">-Name</span></span>
<span data-ttu-id="496a9-122">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="496a9-122">Specifies the management group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a9-123">-Digite</span><span class="sxs-lookup"><span data-stu-id="496a9-123">-Type</span></span>
<span data-ttu-id="496a9-124">Tipo de grupo.</span><span class="sxs-lookup"><span data-stu-id="496a9-124">Group Type.</span></span> <span data-ttu-id="496a9-125">Grupo personalizado é o grupo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="496a9-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="496a9-126">O grupo sistema inclui administrador, desenvolvedores e convidados.</span><span class="sxs-lookup"><span data-stu-id="496a9-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="496a9-127">Não é possível criar ou atualizar um grupo do sistema.</span><span class="sxs-lookup"><span data-stu-id="496a9-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="496a9-128">Grupo externo são grupos do provedor de identidade externa, como o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="496a9-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="496a9-129">Esse parâmetro é opcional e, por padrão, assumido como um grupo personalizado.</span><span class="sxs-lookup"><span data-stu-id="496a9-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: PsApiManagementGroupType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496a9-130">CommonParameters</span></span>
<span data-ttu-id="496a9-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496a9-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="496a9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496a9-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="496a9-133">INPUTS</span></span>

### <span data-ttu-id="496a9-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="496a9-134">None</span></span>
<span data-ttu-id="496a9-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="496a9-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="496a9-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="496a9-136">OUTPUTS</span></span>

### <span data-ttu-id="496a9-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="496a9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="496a9-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="496a9-138">NOTES</span></span>

## <span data-ttu-id="496a9-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="496a9-139">RELATED LINKS</span></span>

[<span data-ttu-id="496a9-140">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="496a9-140">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="496a9-141">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="496a9-141">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="496a9-142">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="496a9-142">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


