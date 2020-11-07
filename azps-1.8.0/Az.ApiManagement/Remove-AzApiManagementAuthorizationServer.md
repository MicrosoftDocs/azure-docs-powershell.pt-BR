---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: cc990e074274917e13b3659aaf0c88f2185f4bf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771387"
---
# <span data-ttu-id="7cca7-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7cca7-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="7cca7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cca7-102">SYNOPSIS</span></span>
<span data-ttu-id="7cca7-103">Remove um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="7cca7-103">Removes an authorization server.</span></span>

## <span data-ttu-id="7cca7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cca7-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cca7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7cca7-105">DESCRIPTION</span></span>
<span data-ttu-id="7cca7-106">O cmdlet **Remove-AzApiManagementAuthorizationServer** remove um servidor de autorização de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="7cca7-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="7cca7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cca7-107">EXAMPLES</span></span>

### <span data-ttu-id="7cca7-108">Exemplo 1: remover um servidor de autorização</span><span class="sxs-lookup"><span data-stu-id="7cca7-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="7cca7-109">Esse comando Remove o servidor de autorização de gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="7cca7-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="7cca7-110">Como o parâmetro *Force* é especificado, nenhuma confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="7cca7-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="7cca7-111">OS</span><span class="sxs-lookup"><span data-stu-id="7cca7-111">PARAMETERS</span></span>

### <span data-ttu-id="7cca7-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7cca7-112">-Context</span></span>
<span data-ttu-id="7cca7-113">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7cca7-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7cca7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cca7-114">-DefaultProfile</span></span>
<span data-ttu-id="7cca7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7cca7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cca7-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cca7-116">-PassThru</span></span>
<span data-ttu-id="7cca7-117">PassThru</span><span class="sxs-lookup"><span data-stu-id="7cca7-117">passthru</span></span>

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

### <span data-ttu-id="7cca7-118">-ServerID</span><span class="sxs-lookup"><span data-stu-id="7cca7-118">-ServerId</span></span>
<span data-ttu-id="7cca7-119">Especifica a ID do servidor de autorização a ser removida.</span><span class="sxs-lookup"><span data-stu-id="7cca7-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="7cca7-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7cca7-120">-Confirm</span></span>
<span data-ttu-id="7cca7-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cca7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cca7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cca7-122">-WhatIf</span></span>
<span data-ttu-id="7cca7-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7cca7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cca7-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7cca7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cca7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cca7-125">CommonParameters</span></span>
<span data-ttu-id="7cca7-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cca7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cca7-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cca7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cca7-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7cca7-128">INPUTS</span></span>

### <span data-ttu-id="7cca7-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7cca7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7cca7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7cca7-130">System.String</span></span>

### <span data-ttu-id="7cca7-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7cca7-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7cca7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7cca7-132">OUTPUTS</span></span>

### <span data-ttu-id="7cca7-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7cca7-133">System.Boolean</span></span>

## <span data-ttu-id="7cca7-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7cca7-134">NOTES</span></span>

## <span data-ttu-id="7cca7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cca7-135">RELATED LINKS</span></span>

[<span data-ttu-id="7cca7-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7cca7-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="7cca7-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7cca7-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="7cca7-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7cca7-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


