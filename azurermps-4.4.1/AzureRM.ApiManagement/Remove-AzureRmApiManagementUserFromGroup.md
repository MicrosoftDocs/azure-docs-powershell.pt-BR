---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: 2867e8eec65de040a0da61a1af960abc9797bb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603412"
---
# <span data-ttu-id="0b3b4-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="0b3b4-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="0b3b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3b4-103">Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b3b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b3b4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b3b4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b3b4-105">DESCRIPTION</span></span>
<span data-ttu-id="0b3b4-106">O cmdlet **Remove-AzureRmApiManagementUserFromGroup** remove um usuário de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="0b3b4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b3b4-107">EXAMPLES</span></span>

### <span data-ttu-id="0b3b4-108">Exemplo 1: remover um usuário de um grupo</span><span class="sxs-lookup"><span data-stu-id="0b3b4-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="0b3b4-109">Esse comando Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="0b3b4-110">OS</span><span class="sxs-lookup"><span data-stu-id="0b3b4-110">PARAMETERS</span></span>

### <span data-ttu-id="0b3b4-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0b3b4-111">-Context</span></span>
<span data-ttu-id="0b3b4-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0b3b4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0b3b4-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0b3b4-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0b3b4-114">-GroupId</span></span>
<span data-ttu-id="0b3b4-115">Especifica a ID do grupo do qual você deseja remover um usuário.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-115">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="0b3b4-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b3b4-116">-PassThru</span></span>
<span data-ttu-id="0b3b4-117">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="0b3b4-118">-UserId</span><span class="sxs-lookup"><span data-stu-id="0b3b4-118">-UserId</span></span>
<span data-ttu-id="0b3b4-119">Especifica a ID do usuário a ser removida do grupo.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-119">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="0b3b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3b4-120">-DefaultProfile</span></span>
<span data-ttu-id="0b3b4-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b3b4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3b4-122">CommonParameters</span></span>
<span data-ttu-id="0b3b4-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3b4-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b3b4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3b4-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b3b4-125">INPUTS</span></span>

## <span data-ttu-id="0b3b4-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b3b4-126">OUTPUTS</span></span>

### <span data-ttu-id="0b3b4-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b3b4-127">System.Boolean</span></span>

## <span data-ttu-id="0b3b4-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b3b4-128">NOTES</span></span>

## <span data-ttu-id="0b3b4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b3b4-129">RELATED LINKS</span></span>

[<span data-ttu-id="0b3b4-130">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="0b3b4-130">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="0b3b4-131">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0b3b4-131">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


