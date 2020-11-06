---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 55a78bbf03ae82b0d861a89dfd6e843399580bef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597994"
---
# <span data-ttu-id="1c7f4-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1c7f4-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="1c7f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c7f4-103">Remove um back-end.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-103">Removes a Backend.</span></span>

## <span data-ttu-id="1c7f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c7f4-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c7f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c7f4-105">DESCRIPTION</span></span>
<span data-ttu-id="1c7f4-106">Remove um back-end especificado pelo identificador do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="1c7f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c7f4-107">EXAMPLES</span></span>

### <span data-ttu-id="1c7f4-108">Exemplo 1: remover o back-end 123</span><span class="sxs-lookup"><span data-stu-id="1c7f4-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="1c7f4-109">OS</span><span class="sxs-lookup"><span data-stu-id="1c7f4-109">PARAMETERS</span></span>

### <span data-ttu-id="1c7f4-110">-Backid</span><span class="sxs-lookup"><span data-stu-id="1c7f4-110">-BackendId</span></span>
<span data-ttu-id="1c7f4-111">Identificador do back-end existente.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-111">Identifier of existing backend.</span></span>
<span data-ttu-id="1c7f4-112">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-112">This parameter is required.</span></span>

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

### <span data-ttu-id="1c7f4-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1c7f4-113">-Context</span></span>
<span data-ttu-id="1c7f4-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1c7f4-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-115">This parameter is required.</span></span>

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

### <span data-ttu-id="1c7f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c7f4-116">-DefaultProfile</span></span>
<span data-ttu-id="1c7f4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c7f4-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c7f4-118">-PassThru</span></span>
<span data-ttu-id="1c7f4-119">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="1c7f4-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-120">This parameter is optional.</span></span>
<span data-ttu-id="1c7f4-121">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-121">Default value is false.</span></span>

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

### <span data-ttu-id="1c7f4-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c7f4-122">-Confirm</span></span>
<span data-ttu-id="1c7f4-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7f4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c7f4-124">-WhatIf</span></span>
<span data-ttu-id="1c7f4-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c7f4-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c7f4-127">CommonParameters</span></span>
<span data-ttu-id="1c7f4-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c7f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c7f4-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c7f4-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c7f4-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c7f4-130">INPUTS</span></span>

### <span data-ttu-id="1c7f4-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1c7f4-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c7f4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1c7f4-132">System.String</span></span>

### <span data-ttu-id="1c7f4-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1c7f4-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1c7f4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c7f4-134">OUTPUTS</span></span>

### <span data-ttu-id="1c7f4-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c7f4-135">System.Boolean</span></span>

## <span data-ttu-id="1c7f4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c7f4-136">NOTES</span></span>

## <span data-ttu-id="1c7f4-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c7f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="1c7f4-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1c7f4-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="1c7f4-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1c7f4-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="1c7f4-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1c7f4-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="1c7f4-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1c7f4-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="1c7f4-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1c7f4-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
