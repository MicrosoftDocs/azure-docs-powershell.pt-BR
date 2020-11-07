---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942127"
---
# <span data-ttu-id="ba9ce-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="ba9ce-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="ba9ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9ce-103">Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="ba9ce-103">Removes a user from a group.</span></span>

## <span data-ttu-id="ba9ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba9ce-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba9ce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba9ce-105">DESCRIPTION</span></span>
<span data-ttu-id="ba9ce-106">O cmdlet **Remove-AzApiManagementUserFromGroup** remove um usuário de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="ba9ce-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="ba9ce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba9ce-107">EXAMPLES</span></span>

### <span data-ttu-id="ba9ce-108">Exemplo 1: remover um usuário de um grupo</span><span class="sxs-lookup"><span data-stu-id="ba9ce-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="ba9ce-109">Esse comando Remove um usuário de um grupo.</span><span class="sxs-lookup"><span data-stu-id="ba9ce-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="ba9ce-110">OS</span><span class="sxs-lookup"><span data-stu-id="ba9ce-110">PARAMETERS</span></span>

### <span data-ttu-id="ba9ce-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ba9ce-111">-Context</span></span>
<span data-ttu-id="ba9ce-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ba9ce-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ba9ce-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ba9ce-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ba9ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9ce-114">-DefaultProfile</span></span>
<span data-ttu-id="ba9ce-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9ce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba9ce-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ba9ce-116">-GroupId</span></span>
<span data-ttu-id="ba9ce-117">Especifica a ID do grupo do qual você deseja remover um usuário.</span><span class="sxs-lookup"><span data-stu-id="ba9ce-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="ba9ce-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba9ce-118">-PassThru</span></span>
<span data-ttu-id="ba9ce-119">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ba9ce-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ba9ce-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="ba9ce-120">-UserId</span></span>
<span data-ttu-id="ba9ce-121">Especifica a ID do usuário a ser removida do grupo.</span><span class="sxs-lookup"><span data-stu-id="ba9ce-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="ba9ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9ce-122">CommonParameters</span></span>
<span data-ttu-id="ba9ce-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba9ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9ce-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba9ce-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9ce-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba9ce-125">INPUTS</span></span>

### <span data-ttu-id="ba9ce-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ba9ce-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ba9ce-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ba9ce-127">System.String</span></span>

### <span data-ttu-id="ba9ce-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ba9ce-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ba9ce-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba9ce-129">OUTPUTS</span></span>

### <span data-ttu-id="ba9ce-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba9ce-130">System.Boolean</span></span>

## <span data-ttu-id="ba9ce-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba9ce-131">NOTES</span></span>

## <span data-ttu-id="ba9ce-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba9ce-132">RELATED LINKS</span></span>

[<span data-ttu-id="ba9ce-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="ba9ce-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="ba9ce-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ba9ce-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


