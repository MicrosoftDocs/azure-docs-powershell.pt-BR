---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 8cbb9afc37242330bc76b7413033dc41cbd61cd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888011"
---
# <span data-ttu-id="ea63d-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ea63d-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="ea63d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea63d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea63d-103">Remove um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="ea63d-103">Removes an authorization server.</span></span>

## <span data-ttu-id="ea63d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ea63d-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea63d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ea63d-105">DESCRIPTION</span></span>
<span data-ttu-id="ea63d-106">O cmdlet **Remove-AzApiManagementAuthorizationServer** remove um servidor de autorização de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea63d-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="ea63d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea63d-107">EXAMPLES</span></span>

### <span data-ttu-id="ea63d-108">Exemplo 1: Remover um servidor de autorização</span><span class="sxs-lookup"><span data-stu-id="ea63d-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="ea63d-109">Este comando remove o Servidor de Autorização de Gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="ea63d-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="ea63d-110">Como o *parâmetro Force* é especificado, nenhuma confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="ea63d-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="ea63d-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ea63d-111">PARAMETERS</span></span>

### <span data-ttu-id="ea63d-112">-Context</span><span class="sxs-lookup"><span data-stu-id="ea63d-112">-Context</span></span>
<span data-ttu-id="ea63d-113">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="ea63d-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ea63d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea63d-114">-DefaultProfile</span></span>
<span data-ttu-id="ea63d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ea63d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea63d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea63d-116">-PassThru</span></span>
<span data-ttu-id="ea63d-117">passthru</span><span class="sxs-lookup"><span data-stu-id="ea63d-117">passthru</span></span>

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

### <span data-ttu-id="ea63d-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="ea63d-118">-ServerId</span></span>
<span data-ttu-id="ea63d-119">Especifica a ID do servidor de autorização a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ea63d-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="ea63d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea63d-120">-Confirm</span></span>
<span data-ttu-id="ea63d-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea63d-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea63d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea63d-122">-WhatIf</span></span>
<span data-ttu-id="ea63d-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea63d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea63d-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea63d-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea63d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea63d-125">CommonParameters</span></span>
<span data-ttu-id="ea63d-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea63d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea63d-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea63d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea63d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea63d-128">INPUTS</span></span>

### <span data-ttu-id="ea63d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ea63d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ea63d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ea63d-130">System.String</span></span>

### <span data-ttu-id="ea63d-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ea63d-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ea63d-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ea63d-132">OUTPUTS</span></span>

### <span data-ttu-id="ea63d-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea63d-133">System.Boolean</span></span>

## <span data-ttu-id="ea63d-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="ea63d-134">NOTES</span></span>

## <span data-ttu-id="ea63d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea63d-135">RELATED LINKS</span></span>

[<span data-ttu-id="ea63d-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ea63d-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="ea63d-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ea63d-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="ea63d-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ea63d-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


