---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: 300c99926ae7f58a6bf53ba49f3b5b86f243e150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609536"
---
# <span data-ttu-id="643d9-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="643d9-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="643d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="643d9-102">SYNOPSIS</span></span>
<span data-ttu-id="643d9-103">Adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="643d9-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="643d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="643d9-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="643d9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="643d9-105">DESCRIPTION</span></span>
<span data-ttu-id="643d9-106">O cmdlet **Add-AzureRmApiManagementUserToGroup** adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="643d9-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="643d9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="643d9-107">EXAMPLES</span></span>

### <span data-ttu-id="643d9-108">Exemplo 1: adicionar um usuário a um grupo</span><span class="sxs-lookup"><span data-stu-id="643d9-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="643d9-109">Esse comando adiciona um usuário existente a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="643d9-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="643d9-110">OS</span><span class="sxs-lookup"><span data-stu-id="643d9-110">PARAMETERS</span></span>

### <span data-ttu-id="643d9-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="643d9-111">-Context</span></span>
<span data-ttu-id="643d9-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="643d9-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="643d9-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="643d9-113">This parameter is required.</span></span>

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

### <span data-ttu-id="643d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643d9-114">-DefaultProfile</span></span>
<span data-ttu-id="643d9-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="643d9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="643d9-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="643d9-116">-GroupId</span></span>
<span data-ttu-id="643d9-117">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="643d9-117">Specifies the group ID.</span></span>
<span data-ttu-id="643d9-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="643d9-118">This parameter is required.</span></span>

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

### <span data-ttu-id="643d9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="643d9-119">-PassThru</span></span>
<span data-ttu-id="643d9-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="643d9-120">passthru</span></span>

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

### <span data-ttu-id="643d9-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="643d9-121">-UserId</span></span>
<span data-ttu-id="643d9-122">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="643d9-122">Specifies the user ID.</span></span>
<span data-ttu-id="643d9-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="643d9-123">This parameter is required.</span></span>

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

### <span data-ttu-id="643d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643d9-124">CommonParameters</span></span>
<span data-ttu-id="643d9-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="643d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643d9-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643d9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643d9-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="643d9-127">INPUTS</span></span>

### <span data-ttu-id="643d9-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="643d9-128">None</span></span>
<span data-ttu-id="643d9-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="643d9-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="643d9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="643d9-130">OUTPUTS</span></span>

### <span data-ttu-id="643d9-131">Booliana</span><span class="sxs-lookup"><span data-stu-id="643d9-131">Boolean</span></span>

## <span data-ttu-id="643d9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="643d9-132">NOTES</span></span>

## <span data-ttu-id="643d9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="643d9-133">RELATED LINKS</span></span>

[<span data-ttu-id="643d9-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="643d9-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="643d9-135">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="643d9-135">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


