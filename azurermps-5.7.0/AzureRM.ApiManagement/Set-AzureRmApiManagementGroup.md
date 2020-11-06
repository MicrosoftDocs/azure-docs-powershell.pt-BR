---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 20f2f79c154cd16dcf09501bdbefb488fdeb61eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430541"
---
# <span data-ttu-id="9c917-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9c917-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="9c917-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c917-102">SYNOPSIS</span></span>
<span data-ttu-id="9c917-103">Configura um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="9c917-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c917-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c917-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c917-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c917-105">DESCRIPTION</span></span>
<span data-ttu-id="9c917-106">O cmdlet **set-AzureRmApiManagementGroup** configura um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="9c917-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="9c917-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c917-107">EXAMPLES</span></span>

### <span data-ttu-id="9c917-108">Exemplo 1: configurar um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="9c917-108">Example 1: Configure a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="9c917-109">Esse comando configura um grupo de gerenciamento chamado Group0001.</span><span class="sxs-lookup"><span data-stu-id="9c917-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="9c917-110">OS</span><span class="sxs-lookup"><span data-stu-id="9c917-110">PARAMETERS</span></span>

### <span data-ttu-id="9c917-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9c917-111">-Context</span></span>
<span data-ttu-id="9c917-112">Especifica uma instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9c917-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9c917-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c917-113">-DefaultProfile</span></span>
<span data-ttu-id="9c917-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c917-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9c917-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9c917-115">-Description</span></span>
<span data-ttu-id="9c917-116">Especifica a descrição do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9c917-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="9c917-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9c917-117">-GroupId</span></span>
<span data-ttu-id="9c917-118">Especifica o identificador do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9c917-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="9c917-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c917-119">-Name</span></span>
<span data-ttu-id="9c917-120">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9c917-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="9c917-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c917-121">-PassThru</span></span>
<span data-ttu-id="9c917-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="9c917-122">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c917-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c917-123">CommonParameters</span></span>
<span data-ttu-id="9c917-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c917-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c917-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c917-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c917-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c917-126">INPUTS</span></span>

### <span data-ttu-id="9c917-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9c917-127">None</span></span>
<span data-ttu-id="9c917-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9c917-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c917-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c917-129">OUTPUTS</span></span>

### <span data-ttu-id="9c917-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9c917-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="9c917-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c917-131">NOTES</span></span>

## <span data-ttu-id="9c917-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c917-132">RELATED LINKS</span></span>

[<span data-ttu-id="9c917-133">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9c917-133">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="9c917-134">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9c917-134">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="9c917-135">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9c917-135">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


