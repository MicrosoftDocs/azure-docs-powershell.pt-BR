---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955202"
---
# <span data-ttu-id="108cd-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="108cd-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="108cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="108cd-102">SYNOPSIS</span></span>
<span data-ttu-id="108cd-103">Adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="108cd-103">Adds a user to a group.</span></span>

## <span data-ttu-id="108cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="108cd-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="108cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="108cd-105">DESCRIPTION</span></span>
<span data-ttu-id="108cd-106">O cmdlet **Add-AzApiManagementUserToGroup** adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="108cd-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="108cd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="108cd-107">EXAMPLES</span></span>

### <span data-ttu-id="108cd-108">Exemplo 1: adicionar um usuário a um grupo</span><span class="sxs-lookup"><span data-stu-id="108cd-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="108cd-109">Esse comando adiciona um usuário existente a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="108cd-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="108cd-110">OS</span><span class="sxs-lookup"><span data-stu-id="108cd-110">PARAMETERS</span></span>

### <span data-ttu-id="108cd-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="108cd-111">-Context</span></span>
<span data-ttu-id="108cd-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="108cd-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="108cd-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="108cd-113">This parameter is required.</span></span>

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

### <span data-ttu-id="108cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108cd-114">-DefaultProfile</span></span>
<span data-ttu-id="108cd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="108cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="108cd-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="108cd-116">-GroupId</span></span>
<span data-ttu-id="108cd-117">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="108cd-117">Specifies the group ID.</span></span>
<span data-ttu-id="108cd-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="108cd-118">This parameter is required.</span></span>

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

### <span data-ttu-id="108cd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="108cd-119">-PassThru</span></span>
<span data-ttu-id="108cd-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="108cd-120">passthru</span></span>

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

### <span data-ttu-id="108cd-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="108cd-121">-UserId</span></span>
<span data-ttu-id="108cd-122">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="108cd-122">Specifies the user ID.</span></span>
<span data-ttu-id="108cd-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="108cd-123">This parameter is required.</span></span>

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

### <span data-ttu-id="108cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108cd-124">CommonParameters</span></span>
<span data-ttu-id="108cd-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="108cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108cd-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="108cd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108cd-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="108cd-127">INPUTS</span></span>

### <span data-ttu-id="108cd-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="108cd-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="108cd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="108cd-129">System.String</span></span>

### <span data-ttu-id="108cd-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="108cd-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="108cd-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="108cd-131">OUTPUTS</span></span>

### <span data-ttu-id="108cd-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="108cd-132">System.Boolean</span></span>

## <span data-ttu-id="108cd-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="108cd-133">NOTES</span></span>

## <span data-ttu-id="108cd-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="108cd-134">RELATED LINKS</span></span>

[<span data-ttu-id="108cd-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="108cd-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="108cd-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="108cd-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


