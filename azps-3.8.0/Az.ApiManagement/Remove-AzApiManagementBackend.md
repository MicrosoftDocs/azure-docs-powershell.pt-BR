---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: d1a353e9534cbfd2530bb67f5eeda92fbb6d72ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943011"
---
# <span data-ttu-id="53b0c-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="53b0c-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="53b0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="53b0c-103">Remove um back-end.</span><span class="sxs-lookup"><span data-stu-id="53b0c-103">Removes a Backend.</span></span>

## <span data-ttu-id="53b0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53b0c-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53b0c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="53b0c-106">Remove um back-end especificado pelo identificador do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="53b0c-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="53b0c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="53b0c-108">Exemplo 1: remover o back-end 123</span><span class="sxs-lookup"><span data-stu-id="53b0c-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="53b0c-109">OS</span><span class="sxs-lookup"><span data-stu-id="53b0c-109">PARAMETERS</span></span>

### <span data-ttu-id="53b0c-110">-Backid</span><span class="sxs-lookup"><span data-stu-id="53b0c-110">-BackendId</span></span>
<span data-ttu-id="53b0c-111">Identificador do back-end existente.</span><span class="sxs-lookup"><span data-stu-id="53b0c-111">Identifier of existing backend.</span></span>
<span data-ttu-id="53b0c-112">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="53b0c-112">This parameter is required.</span></span>

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

### <span data-ttu-id="53b0c-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="53b0c-113">-Context</span></span>
<span data-ttu-id="53b0c-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="53b0c-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="53b0c-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="53b0c-115">This parameter is required.</span></span>

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

### <span data-ttu-id="53b0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b0c-116">-DefaultProfile</span></span>
<span data-ttu-id="53b0c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53b0c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53b0c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53b0c-118">-PassThru</span></span>
<span data-ttu-id="53b0c-119">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="53b0c-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="53b0c-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="53b0c-120">This parameter is optional.</span></span>
<span data-ttu-id="53b0c-121">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="53b0c-121">Default value is false.</span></span>

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

### <span data-ttu-id="53b0c-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53b0c-122">-Confirm</span></span>
<span data-ttu-id="53b0c-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53b0c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53b0c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53b0c-124">-WhatIf</span></span>
<span data-ttu-id="53b0c-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53b0c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53b0c-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53b0c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53b0c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b0c-127">CommonParameters</span></span>
<span data-ttu-id="53b0c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b0c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b0c-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53b0c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b0c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53b0c-130">INPUTS</span></span>

### <span data-ttu-id="53b0c-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="53b0c-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="53b0c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="53b0c-132">System.String</span></span>

### <span data-ttu-id="53b0c-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="53b0c-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="53b0c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53b0c-134">OUTPUTS</span></span>

### <span data-ttu-id="53b0c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53b0c-135">System.Boolean</span></span>

## <span data-ttu-id="53b0c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53b0c-136">NOTES</span></span>

## <span data-ttu-id="53b0c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53b0c-137">RELATED LINKS</span></span>

[<span data-ttu-id="53b0c-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="53b0c-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="53b0c-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="53b0c-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="53b0c-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="53b0c-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="53b0c-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="53b0c-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="53b0c-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="53b0c-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
