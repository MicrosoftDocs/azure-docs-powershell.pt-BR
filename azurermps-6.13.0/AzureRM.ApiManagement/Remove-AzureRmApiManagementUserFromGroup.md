---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: abf9cab8e7e832a6221a25aff40f4d7b7ae55d58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609447"
---
# <span data-ttu-id="9122c-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="9122c-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="9122c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9122c-102">SYNOPSIS</span></span>
<span data-ttu-id="9122c-103">Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="9122c-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9122c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9122c-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9122c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9122c-105">DESCRIPTION</span></span>
<span data-ttu-id="9122c-106">O cmdlet **Remove-AzureRmApiManagementUserFromGroup** remove um usuário de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="9122c-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="9122c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9122c-107">EXAMPLES</span></span>

### <span data-ttu-id="9122c-108">Exemplo 1: remover um usuário de um grupo</span><span class="sxs-lookup"><span data-stu-id="9122c-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="9122c-109">Esse comando Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="9122c-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="9122c-110">OS</span><span class="sxs-lookup"><span data-stu-id="9122c-110">PARAMETERS</span></span>

### <span data-ttu-id="9122c-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9122c-111">-Context</span></span>
<span data-ttu-id="9122c-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9122c-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9122c-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9122c-113">This parameter is required.</span></span>

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

### <span data-ttu-id="9122c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9122c-114">-DefaultProfile</span></span>
<span data-ttu-id="9122c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9122c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9122c-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9122c-116">-GroupId</span></span>
<span data-ttu-id="9122c-117">Especifica a ID do grupo do qual você deseja remover um usuário.</span><span class="sxs-lookup"><span data-stu-id="9122c-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="9122c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9122c-118">-PassThru</span></span>
<span data-ttu-id="9122c-119">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9122c-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="9122c-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="9122c-120">-UserId</span></span>
<span data-ttu-id="9122c-121">Especifica a ID do usuário a ser removida do grupo.</span><span class="sxs-lookup"><span data-stu-id="9122c-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="9122c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9122c-122">CommonParameters</span></span>
<span data-ttu-id="9122c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9122c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9122c-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9122c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9122c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9122c-125">INPUTS</span></span>

### <span data-ttu-id="9122c-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9122c-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9122c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9122c-127">System.String</span></span>

### <span data-ttu-id="9122c-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9122c-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9122c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9122c-129">OUTPUTS</span></span>

### <span data-ttu-id="9122c-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9122c-130">System.Boolean</span></span>

## <span data-ttu-id="9122c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9122c-131">NOTES</span></span>

## <span data-ttu-id="9122c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9122c-132">RELATED LINKS</span></span>

[<span data-ttu-id="9122c-133">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="9122c-133">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="9122c-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9122c-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


