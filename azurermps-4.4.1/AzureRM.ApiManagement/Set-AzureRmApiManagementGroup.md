---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 99c5cef4a15619da455b3e7ba1c7891652b991f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440227"
---
# <span data-ttu-id="31758-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="31758-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="31758-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31758-102">SYNOPSIS</span></span>
<span data-ttu-id="31758-103">Configura um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="31758-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31758-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31758-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31758-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31758-105">DESCRIPTION</span></span>
<span data-ttu-id="31758-106">O cmdlet **set-AzureRmApiManagementGroup** configura um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="31758-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="31758-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31758-107">EXAMPLES</span></span>

### <span data-ttu-id="31758-108">Exemplo 1: configurar um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="31758-108">Example 1: Configure a management group</span></span>
```
PS C:\>Set-AzureRmApiManagementGroup -Context $APImContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="31758-109">Esse comando configura um grupo de gerenciamento chamado Group0001.</span><span class="sxs-lookup"><span data-stu-id="31758-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="31758-110">OS</span><span class="sxs-lookup"><span data-stu-id="31758-110">PARAMETERS</span></span>

### <span data-ttu-id="31758-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="31758-111">-Context</span></span>
<span data-ttu-id="31758-112">Especifica uma instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="31758-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="31758-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="31758-113">-Description</span></span>
<span data-ttu-id="31758-114">Especifica a descrição do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="31758-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="31758-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="31758-115">-GroupId</span></span>
<span data-ttu-id="31758-116">Especifica o identificador do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="31758-116">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="31758-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="31758-117">-Name</span></span>
<span data-ttu-id="31758-118">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="31758-118">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="31758-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31758-119">-PassThru</span></span>
<span data-ttu-id="31758-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="31758-120">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31758-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31758-121">-DefaultProfile</span></span>
<span data-ttu-id="31758-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31758-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31758-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31758-123">CommonParameters</span></span>
<span data-ttu-id="31758-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31758-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31758-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31758-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31758-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31758-126">INPUTS</span></span>

## <span data-ttu-id="31758-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31758-127">OUTPUTS</span></span>

### <span data-ttu-id="31758-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="31758-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="31758-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31758-129">NOTES</span></span>

## <span data-ttu-id="31758-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31758-130">RELATED LINKS</span></span>

[<span data-ttu-id="31758-131">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="31758-131">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="31758-132">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="31758-132">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="31758-133">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="31758-133">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


