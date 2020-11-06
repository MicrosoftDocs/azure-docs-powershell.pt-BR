---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 11adcd1bf7f16b9c67dadfda9377fd0aa5b3d138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598141"
---
# <span data-ttu-id="2d537-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="2d537-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="2d537-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d537-102">SYNOPSIS</span></span>
<span data-ttu-id="2d537-103">Adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="2d537-103">Adds a user to a group.</span></span>

## <span data-ttu-id="2d537-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d537-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d537-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d537-105">DESCRIPTION</span></span>
<span data-ttu-id="2d537-106">O cmdlet **Add-AzApiManagementUserToGroup** adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="2d537-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="2d537-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d537-107">EXAMPLES</span></span>

### <span data-ttu-id="2d537-108">Exemplo 1: adicionar um usuário a um grupo</span><span class="sxs-lookup"><span data-stu-id="2d537-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="2d537-109">Esse comando adiciona um usuário existente a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="2d537-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="2d537-110">OS</span><span class="sxs-lookup"><span data-stu-id="2d537-110">PARAMETERS</span></span>

### <span data-ttu-id="2d537-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2d537-111">-Context</span></span>
<span data-ttu-id="2d537-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2d537-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2d537-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2d537-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2d537-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d537-114">-DefaultProfile</span></span>
<span data-ttu-id="2d537-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d537-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d537-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2d537-116">-GroupId</span></span>
<span data-ttu-id="2d537-117">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="2d537-117">Specifies the group ID.</span></span>
<span data-ttu-id="2d537-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2d537-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2d537-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d537-119">-PassThru</span></span>
<span data-ttu-id="2d537-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="2d537-120">passthru</span></span>

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

### <span data-ttu-id="2d537-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="2d537-121">-UserId</span></span>
<span data-ttu-id="2d537-122">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="2d537-122">Specifies the user ID.</span></span>
<span data-ttu-id="2d537-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2d537-123">This parameter is required.</span></span>

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

### <span data-ttu-id="2d537-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d537-124">CommonParameters</span></span>
<span data-ttu-id="2d537-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d537-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d537-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d537-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d537-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d537-127">INPUTS</span></span>

### <span data-ttu-id="2d537-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2d537-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2d537-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2d537-129">System.String</span></span>

### <span data-ttu-id="2d537-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2d537-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2d537-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d537-131">OUTPUTS</span></span>

### <span data-ttu-id="2d537-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d537-132">System.Boolean</span></span>

## <span data-ttu-id="2d537-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d537-133">NOTES</span></span>

## <span data-ttu-id="2d537-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d537-134">RELATED LINKS</span></span>

[<span data-ttu-id="2d537-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2d537-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="2d537-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="2d537-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


