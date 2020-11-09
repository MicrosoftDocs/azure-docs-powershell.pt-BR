---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281537"
---
# <span data-ttu-id="7f2e8-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="7f2e8-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="7f2e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f2e8-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2e8-103">Adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-103">Adds a user to a group.</span></span>

## <span data-ttu-id="7f2e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f2e8-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f2e8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f2e8-105">DESCRIPTION</span></span>
<span data-ttu-id="7f2e8-106">O cmdlet **Add-AzApiManagementUserToGroup** adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="7f2e8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f2e8-107">EXAMPLES</span></span>

### <span data-ttu-id="7f2e8-108">Exemplo 1: adicionar um usuário a um grupo</span><span class="sxs-lookup"><span data-stu-id="7f2e8-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="7f2e8-109">Esse comando adiciona um usuário existente a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="7f2e8-110">OS</span><span class="sxs-lookup"><span data-stu-id="7f2e8-110">PARAMETERS</span></span>

### <span data-ttu-id="7f2e8-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7f2e8-111">-Context</span></span>
<span data-ttu-id="7f2e8-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7f2e8-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="7f2e8-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7f2e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2e8-114">-DefaultProfile</span></span>
<span data-ttu-id="7f2e8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f2e8-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="7f2e8-116">-GroupId</span></span>
<span data-ttu-id="7f2e8-117">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-117">Specifies the group ID.</span></span>
<span data-ttu-id="7f2e8-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-118">This parameter is required.</span></span>

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

### <span data-ttu-id="7f2e8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f2e8-119">-PassThru</span></span>
<span data-ttu-id="7f2e8-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="7f2e8-120">passthru</span></span>

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

### <span data-ttu-id="7f2e8-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="7f2e8-121">-UserId</span></span>
<span data-ttu-id="7f2e8-122">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-122">Specifies the user ID.</span></span>
<span data-ttu-id="7f2e8-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-123">This parameter is required.</span></span>

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

### <span data-ttu-id="7f2e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2e8-124">CommonParameters</span></span>
<span data-ttu-id="7f2e8-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f2e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2e8-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f2e8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2e8-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f2e8-127">INPUTS</span></span>

### <span data-ttu-id="7f2e8-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7f2e8-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7f2e8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7f2e8-129">System.String</span></span>

### <span data-ttu-id="7f2e8-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f2e8-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f2e8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f2e8-131">OUTPUTS</span></span>

### <span data-ttu-id="7f2e8-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f2e8-132">System.Boolean</span></span>

## <span data-ttu-id="7f2e8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f2e8-133">NOTES</span></span>

## <span data-ttu-id="7f2e8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f2e8-134">RELATED LINKS</span></span>

[<span data-ttu-id="7f2e8-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7f2e8-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="7f2e8-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="7f2e8-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


