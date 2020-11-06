---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: bdcbac04d621319ac3837f1efaef52018e0f4eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441506"
---
# <span data-ttu-id="f868b-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="f868b-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="f868b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f868b-102">SYNOPSIS</span></span>
<span data-ttu-id="f868b-103">Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="f868b-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f868b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f868b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f868b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f868b-105">DESCRIPTION</span></span>
<span data-ttu-id="f868b-106">O cmdlet **Remove-AzureRmApiManagementUserFromGroup** remove um usuário de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="f868b-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="f868b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f868b-107">EXAMPLES</span></span>

### <span data-ttu-id="f868b-108">Exemplo 1: remover um usuário de um grupo</span><span class="sxs-lookup"><span data-stu-id="f868b-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="f868b-109">Esse comando Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="f868b-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="f868b-110">OS</span><span class="sxs-lookup"><span data-stu-id="f868b-110">PARAMETERS</span></span>

### <span data-ttu-id="f868b-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f868b-111">-Context</span></span>
<span data-ttu-id="f868b-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f868b-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f868b-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f868b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f868b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f868b-114">-DefaultProfile</span></span>
<span data-ttu-id="f868b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f868b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f868b-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f868b-116">-GroupId</span></span>
<span data-ttu-id="f868b-117">Especifica a ID do grupo do qual você deseja remover um usuário.</span><span class="sxs-lookup"><span data-stu-id="f868b-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="f868b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f868b-118">-PassThru</span></span>
<span data-ttu-id="f868b-119">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f868b-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="f868b-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="f868b-120">-UserId</span></span>
<span data-ttu-id="f868b-121">Especifica a ID do usuário a ser removida do grupo.</span><span class="sxs-lookup"><span data-stu-id="f868b-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="f868b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f868b-122">CommonParameters</span></span>
<span data-ttu-id="f868b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f868b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f868b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f868b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f868b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f868b-125">INPUTS</span></span>

### <span data-ttu-id="f868b-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f868b-126">None</span></span>
<span data-ttu-id="f868b-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f868b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f868b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f868b-128">OUTPUTS</span></span>

### <span data-ttu-id="f868b-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f868b-129">System.Boolean</span></span>

## <span data-ttu-id="f868b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f868b-130">NOTES</span></span>

## <span data-ttu-id="f868b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f868b-131">RELATED LINKS</span></span>

[<span data-ttu-id="f868b-132">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="f868b-132">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="f868b-133">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f868b-133">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


