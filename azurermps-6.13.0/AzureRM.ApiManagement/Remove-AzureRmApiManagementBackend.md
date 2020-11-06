---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: ef00a5140dc25065c05494211721c5773a9b5243
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426500"
---
# <span data-ttu-id="f9505-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f9505-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="f9505-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9505-102">SYNOPSIS</span></span>
<span data-ttu-id="f9505-103">Remove um back-end.</span><span class="sxs-lookup"><span data-stu-id="f9505-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9505-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9505-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9505-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9505-105">DESCRIPTION</span></span>
<span data-ttu-id="f9505-106">Remove um back-end especificado pelo identificador do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f9505-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="f9505-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9505-107">EXAMPLES</span></span>

### <span data-ttu-id="f9505-108">Exemplo 1: remover o back-end 123</span><span class="sxs-lookup"><span data-stu-id="f9505-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="f9505-109">OS</span><span class="sxs-lookup"><span data-stu-id="f9505-109">PARAMETERS</span></span>

### <span data-ttu-id="f9505-110">-Backid</span><span class="sxs-lookup"><span data-stu-id="f9505-110">-BackendId</span></span>
<span data-ttu-id="f9505-111">Identificador do back-end existente.</span><span class="sxs-lookup"><span data-stu-id="f9505-111">Identifier of existing backend.</span></span>
<span data-ttu-id="f9505-112">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f9505-112">This parameter is required.</span></span>

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

### <span data-ttu-id="f9505-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f9505-113">-Context</span></span>
<span data-ttu-id="f9505-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f9505-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f9505-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f9505-115">This parameter is required.</span></span>

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

### <span data-ttu-id="f9505-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9505-116">-DefaultProfile</span></span>
<span data-ttu-id="f9505-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9505-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9505-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9505-118">-PassThru</span></span>
<span data-ttu-id="f9505-119">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f9505-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="f9505-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f9505-120">This parameter is optional.</span></span>
<span data-ttu-id="f9505-121">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="f9505-121">Default value is false.</span></span>

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

### <span data-ttu-id="f9505-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9505-122">-Confirm</span></span>
<span data-ttu-id="f9505-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9505-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9505-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9505-124">-WhatIf</span></span>
<span data-ttu-id="f9505-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9505-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9505-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9505-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9505-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9505-127">CommonParameters</span></span>
<span data-ttu-id="f9505-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9505-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9505-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9505-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9505-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9505-130">INPUTS</span></span>

### <span data-ttu-id="f9505-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f9505-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f9505-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f9505-132">System.String</span></span>

### <span data-ttu-id="f9505-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9505-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f9505-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9505-134">OUTPUTS</span></span>

### <span data-ttu-id="f9505-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9505-135">System.Boolean</span></span>

## <span data-ttu-id="f9505-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9505-136">NOTES</span></span>

## <span data-ttu-id="f9505-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9505-137">RELATED LINKS</span></span>

[<span data-ttu-id="f9505-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f9505-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="f9505-139">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f9505-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="f9505-140">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="f9505-140">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="f9505-141">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="f9505-141">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="f9505-142">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f9505-142">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
