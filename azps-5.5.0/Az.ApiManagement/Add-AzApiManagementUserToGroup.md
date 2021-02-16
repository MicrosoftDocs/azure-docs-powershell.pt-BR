---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113661"
---
# <span data-ttu-id="0cf91-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="0cf91-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="0cf91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cf91-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf91-103">Adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="0cf91-103">Adds a user to a group.</span></span>

## <span data-ttu-id="0cf91-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cf91-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf91-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cf91-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf91-106">O **cmdlet Add-AzApiManagementUserToGroup** adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="0cf91-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="0cf91-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0cf91-107">EXAMPLES</span></span>

### <span data-ttu-id="0cf91-108">Exemplo 1: Adicionar um usuário a um grupo</span><span class="sxs-lookup"><span data-stu-id="0cf91-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="0cf91-109">Esse comando adiciona um usuário existente a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="0cf91-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="0cf91-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cf91-110">PARAMETERS</span></span>

### <span data-ttu-id="0cf91-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0cf91-111">-Context</span></span>
<span data-ttu-id="0cf91-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="0cf91-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0cf91-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="0cf91-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0cf91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf91-114">-DefaultProfile</span></span>
<span data-ttu-id="0cf91-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0cf91-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cf91-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0cf91-116">-GroupId</span></span>
<span data-ttu-id="0cf91-117">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="0cf91-117">Specifies the group ID.</span></span>
<span data-ttu-id="0cf91-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="0cf91-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0cf91-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cf91-119">-PassThru</span></span>
<span data-ttu-id="0cf91-120">Passthru</span><span class="sxs-lookup"><span data-stu-id="0cf91-120">passthru</span></span>

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

### <span data-ttu-id="0cf91-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="0cf91-121">-UserId</span></span>
<span data-ttu-id="0cf91-122">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="0cf91-122">Specifies the user ID.</span></span>
<span data-ttu-id="0cf91-123">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="0cf91-123">This parameter is required.</span></span>

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

### <span data-ttu-id="0cf91-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf91-124">CommonParameters</span></span>
<span data-ttu-id="0cf91-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf91-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf91-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cf91-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf91-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="0cf91-127">INPUTS</span></span>

### <span data-ttu-id="0cf91-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0cf91-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0cf91-129">System.String</span><span class="sxs-lookup"><span data-stu-id="0cf91-129">System.String</span></span>

### <span data-ttu-id="0cf91-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0cf91-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0cf91-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="0cf91-131">OUTPUTS</span></span>

### <span data-ttu-id="0cf91-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0cf91-132">System.Boolean</span></span>

## <span data-ttu-id="0cf91-133">Notas</span><span class="sxs-lookup"><span data-stu-id="0cf91-133">NOTES</span></span>

## <span data-ttu-id="0cf91-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cf91-134">RELATED LINKS</span></span>

[<span data-ttu-id="0cf91-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0cf91-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="0cf91-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="0cf91-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


