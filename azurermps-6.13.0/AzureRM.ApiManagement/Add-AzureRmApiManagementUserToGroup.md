---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: abb86f40c9ac4a2ca04e0f14500df6c39e550dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432831"
---
# <span data-ttu-id="93074-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="93074-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="93074-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93074-102">SYNOPSIS</span></span>
<span data-ttu-id="93074-103">Adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="93074-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93074-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93074-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93074-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93074-105">DESCRIPTION</span></span>
<span data-ttu-id="93074-106">O cmdlet **Add-AzureRmApiManagementUserToGroup** adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="93074-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="93074-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93074-107">EXAMPLES</span></span>

### <span data-ttu-id="93074-108">Exemplo 1: adicionar um usuário a um grupo</span><span class="sxs-lookup"><span data-stu-id="93074-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="93074-109">Esse comando adiciona um usuário existente a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="93074-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="93074-110">OS</span><span class="sxs-lookup"><span data-stu-id="93074-110">PARAMETERS</span></span>

### <span data-ttu-id="93074-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="93074-111">-Context</span></span>
<span data-ttu-id="93074-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="93074-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="93074-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="93074-113">This parameter is required.</span></span>

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

### <span data-ttu-id="93074-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93074-114">-DefaultProfile</span></span>
<span data-ttu-id="93074-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93074-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93074-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="93074-116">-GroupId</span></span>
<span data-ttu-id="93074-117">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="93074-117">Specifies the group ID.</span></span>
<span data-ttu-id="93074-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="93074-118">This parameter is required.</span></span>

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

### <span data-ttu-id="93074-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93074-119">-PassThru</span></span>
<span data-ttu-id="93074-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="93074-120">passthru</span></span>

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

### <span data-ttu-id="93074-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="93074-121">-UserId</span></span>
<span data-ttu-id="93074-122">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="93074-122">Specifies the user ID.</span></span>
<span data-ttu-id="93074-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="93074-123">This parameter is required.</span></span>

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

### <span data-ttu-id="93074-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93074-124">CommonParameters</span></span>
<span data-ttu-id="93074-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93074-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93074-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93074-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93074-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93074-127">INPUTS</span></span>

### <span data-ttu-id="93074-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="93074-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="93074-129">System. String</span><span class="sxs-lookup"><span data-stu-id="93074-129">System.String</span></span>

### <span data-ttu-id="93074-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93074-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93074-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93074-131">OUTPUTS</span></span>

### <span data-ttu-id="93074-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93074-132">System.Boolean</span></span>

## <span data-ttu-id="93074-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93074-133">NOTES</span></span>

## <span data-ttu-id="93074-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93074-134">RELATED LINKS</span></span>

[<span data-ttu-id="93074-135">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="93074-135">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="93074-136">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="93074-136">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


