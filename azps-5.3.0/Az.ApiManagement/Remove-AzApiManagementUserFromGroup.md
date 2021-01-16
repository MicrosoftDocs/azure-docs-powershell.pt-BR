---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272135"
---
# <span data-ttu-id="2f427-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="2f427-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="2f427-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f427-102">SYNOPSIS</span></span>
<span data-ttu-id="2f427-103">Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="2f427-103">Removes a user from a group.</span></span>

## <span data-ttu-id="2f427-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f427-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f427-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f427-105">DESCRIPTION</span></span>
<span data-ttu-id="2f427-106">O cmdlet **Remove-AzApiManagementUserFromGroup** remove um usuário de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="2f427-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="2f427-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f427-107">EXAMPLES</span></span>

### <span data-ttu-id="2f427-108">Exemplo 1: remover um usuário de um grupo</span><span class="sxs-lookup"><span data-stu-id="2f427-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="2f427-109">Esse comando Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="2f427-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="2f427-110">OS</span><span class="sxs-lookup"><span data-stu-id="2f427-110">PARAMETERS</span></span>

### <span data-ttu-id="2f427-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2f427-111">-Context</span></span>
<span data-ttu-id="2f427-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2f427-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2f427-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2f427-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f427-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f427-114">-DefaultProfile</span></span>
<span data-ttu-id="2f427-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f427-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f427-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2f427-116">-GroupId</span></span>
<span data-ttu-id="2f427-117">Especifica a ID do grupo do qual você deseja remover um usuário.</span><span class="sxs-lookup"><span data-stu-id="2f427-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="2f427-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f427-118">-PassThru</span></span>
<span data-ttu-id="2f427-119">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2f427-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="2f427-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="2f427-120">-UserId</span></span>
<span data-ttu-id="2f427-121">Especifica a ID do usuário a ser removida do grupo.</span><span class="sxs-lookup"><span data-stu-id="2f427-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="2f427-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f427-122">CommonParameters</span></span>
<span data-ttu-id="2f427-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f427-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f427-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f427-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f427-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f427-125">INPUTS</span></span>

### <span data-ttu-id="2f427-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2f427-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2f427-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2f427-127">System.String</span></span>

### <span data-ttu-id="2f427-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2f427-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f427-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f427-129">OUTPUTS</span></span>

### <span data-ttu-id="2f427-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f427-130">System.Boolean</span></span>

## <span data-ttu-id="2f427-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f427-131">NOTES</span></span>

## <span data-ttu-id="2f427-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f427-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f427-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="2f427-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="2f427-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2f427-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


