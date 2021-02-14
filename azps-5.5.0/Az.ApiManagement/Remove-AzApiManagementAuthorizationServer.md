---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117039"
---
# <span data-ttu-id="152d9-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="152d9-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="152d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="152d9-102">SYNOPSIS</span></span>
<span data-ttu-id="152d9-103">Remove um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="152d9-103">Removes an authorization server.</span></span>

## <span data-ttu-id="152d9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="152d9-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="152d9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="152d9-105">DESCRIPTION</span></span>
<span data-ttu-id="152d9-106">O cmdlet **Remove-AzApiManagementAuthorizationServer** remove um servidor de autorização do Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="152d9-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="152d9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="152d9-107">EXAMPLES</span></span>

### <span data-ttu-id="152d9-108">Exemplo 1: Remover um servidor de autorização</span><span class="sxs-lookup"><span data-stu-id="152d9-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="152d9-109">Esse comando remove o Servidor de Autorização de Gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="152d9-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="152d9-110">Como o *parâmetro Forçar* é especificado, nenhuma confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="152d9-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="152d9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="152d9-111">PARAMETERS</span></span>

### <span data-ttu-id="152d9-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="152d9-112">-Context</span></span>
<span data-ttu-id="152d9-113">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="152d9-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="152d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152d9-114">-DefaultProfile</span></span>
<span data-ttu-id="152d9-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="152d9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="152d9-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="152d9-116">-PassThru</span></span>
<span data-ttu-id="152d9-117">Passthru</span><span class="sxs-lookup"><span data-stu-id="152d9-117">passthru</span></span>

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

### <span data-ttu-id="152d9-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="152d9-118">-ServerId</span></span>
<span data-ttu-id="152d9-119">Especifica a ID do servidor de autorização a ser removido.</span><span class="sxs-lookup"><span data-stu-id="152d9-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="152d9-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="152d9-120">-Confirm</span></span>
<span data-ttu-id="152d9-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="152d9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="152d9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152d9-122">-WhatIf</span></span>
<span data-ttu-id="152d9-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="152d9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152d9-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="152d9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="152d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152d9-125">CommonParameters</span></span>
<span data-ttu-id="152d9-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="152d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152d9-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="152d9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152d9-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="152d9-128">INPUTS</span></span>

### <span data-ttu-id="152d9-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="152d9-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="152d9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="152d9-130">System.String</span></span>

### <span data-ttu-id="152d9-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="152d9-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="152d9-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="152d9-132">OUTPUTS</span></span>

### <span data-ttu-id="152d9-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="152d9-133">System.Boolean</span></span>

## <span data-ttu-id="152d9-134">Notas</span><span class="sxs-lookup"><span data-stu-id="152d9-134">NOTES</span></span>

## <span data-ttu-id="152d9-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="152d9-135">RELATED LINKS</span></span>

[<span data-ttu-id="152d9-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="152d9-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="152d9-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="152d9-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="152d9-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="152d9-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


