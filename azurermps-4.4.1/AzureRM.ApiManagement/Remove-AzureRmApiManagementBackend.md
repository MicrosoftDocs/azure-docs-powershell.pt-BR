---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428321"
---
# <span data-ttu-id="555db-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="555db-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="555db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="555db-102">SYNOPSIS</span></span>
<span data-ttu-id="555db-103">Remove um back-end.</span><span class="sxs-lookup"><span data-stu-id="555db-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="555db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="555db-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="555db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="555db-105">DESCRIPTION</span></span>
<span data-ttu-id="555db-106">Remove um back-end especificado pelo identificador do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="555db-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="555db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="555db-107">EXAMPLES</span></span>

### <span data-ttu-id="555db-108">Exemplo 1: remover o back-end 123</span><span class="sxs-lookup"><span data-stu-id="555db-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="555db-109">OS</span><span class="sxs-lookup"><span data-stu-id="555db-109">PARAMETERS</span></span>

### <span data-ttu-id="555db-110">-Backid</span><span class="sxs-lookup"><span data-stu-id="555db-110">-BackendId</span></span>
<span data-ttu-id="555db-111">Identificador do back-end existente.</span><span class="sxs-lookup"><span data-stu-id="555db-111">Identifier of existing backend.</span></span>
<span data-ttu-id="555db-112">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="555db-112">This parameter is required.</span></span>

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

### <span data-ttu-id="555db-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="555db-113">-Context</span></span>
<span data-ttu-id="555db-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="555db-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="555db-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="555db-115">This parameter is required.</span></span>

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

### <span data-ttu-id="555db-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="555db-116">-PassThru</span></span>
<span data-ttu-id="555db-117">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="555db-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="555db-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="555db-118">This parameter is optional.</span></span>
<span data-ttu-id="555db-119">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="555db-119">Default value is false.</span></span>

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

### <span data-ttu-id="555db-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="555db-120">-Confirm</span></span>
<span data-ttu-id="555db-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="555db-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="555db-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="555db-122">-WhatIf</span></span>
<span data-ttu-id="555db-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="555db-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="555db-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="555db-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="555db-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555db-125">-DefaultProfile</span></span>
<span data-ttu-id="555db-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="555db-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="555db-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555db-127">CommonParameters</span></span>
<span data-ttu-id="555db-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="555db-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555db-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="555db-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555db-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="555db-130">INPUTS</span></span>

## <span data-ttu-id="555db-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="555db-131">OUTPUTS</span></span>

### <span data-ttu-id="555db-132">bool</span><span class="sxs-lookup"><span data-stu-id="555db-132">bool</span></span>

## <span data-ttu-id="555db-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="555db-133">NOTES</span></span>

## <span data-ttu-id="555db-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="555db-134">RELATED LINKS</span></span>

[<span data-ttu-id="555db-135">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="555db-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="555db-136">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="555db-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="555db-137">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="555db-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="555db-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="555db-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="555db-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="555db-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
