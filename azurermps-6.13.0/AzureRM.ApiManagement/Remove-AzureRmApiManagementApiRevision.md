---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426503"
---
# <span data-ttu-id="a3adf-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a3adf-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="a3adf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3adf-102">SYNOPSIS</span></span>
<span data-ttu-id="a3adf-103">Revisão de API específica removida</span><span class="sxs-lookup"><span data-stu-id="a3adf-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3adf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3adf-104">SYNTAX</span></span>

### <span data-ttu-id="a3adf-105">ByApiId (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3adf-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3adf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a3adf-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3adf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3adf-107">DESCRIPTION</span></span>
<span data-ttu-id="a3adf-108">O cmdlet **Remove-AzureRmApiManagementApiRevision** remove uma revisão de API específica.</span><span class="sxs-lookup"><span data-stu-id="a3adf-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="a3adf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3adf-109">EXAMPLES</span></span>

### <span data-ttu-id="a3adf-110">Exemplo 1: remover uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="a3adf-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="a3adf-111">Esse comando Remove a `2` revisão da API `echo-api` do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a3adf-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="a3adf-112">OS</span><span class="sxs-lookup"><span data-stu-id="a3adf-112">PARAMETERS</span></span>

### <span data-ttu-id="a3adf-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a3adf-113">-ApiId</span></span>
<span data-ttu-id="a3adf-114">Identificador da API.</span><span class="sxs-lookup"><span data-stu-id="a3adf-114">Identifier of the API.</span></span>
<span data-ttu-id="a3adf-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a3adf-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3adf-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a3adf-116">-ApiRevision</span></span>
<span data-ttu-id="a3adf-117">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="a3adf-117">Identifier of the API Revision.</span></span> <span data-ttu-id="a3adf-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a3adf-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3adf-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a3adf-119">-Context</span></span>
<span data-ttu-id="a3adf-120">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a3adf-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a3adf-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a3adf-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3adf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3adf-122">-DefaultProfile</span></span>
<span data-ttu-id="a3adf-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3adf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3adf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3adf-124">-InputObject</span></span>
<span data-ttu-id="a3adf-125">Instância do PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="a3adf-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="a3adf-126">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a3adf-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3adf-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3adf-127">-PassThru</span></span>
<span data-ttu-id="a3adf-128">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a3adf-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a3adf-129">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a3adf-129">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3adf-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3adf-130">-Confirm</span></span>
<span data-ttu-id="a3adf-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3adf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3adf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3adf-132">-WhatIf</span></span>
<span data-ttu-id="a3adf-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3adf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3adf-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3adf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3adf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3adf-135">CommonParameters</span></span>
<span data-ttu-id="a3adf-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3adf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3adf-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3adf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3adf-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3adf-138">INPUTS</span></span>

### <span data-ttu-id="a3adf-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a3adf-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a3adf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a3adf-140">System.String</span></span>

### <span data-ttu-id="a3adf-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a3adf-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="a3adf-142">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3adf-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a3adf-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3adf-143">OUTPUTS</span></span>

### <span data-ttu-id="a3adf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3adf-144">System.Boolean</span></span>

## <span data-ttu-id="a3adf-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3adf-145">NOTES</span></span>

## <span data-ttu-id="a3adf-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3adf-146">RELATED LINKS</span></span>

[<span data-ttu-id="a3adf-147">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a3adf-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="a3adf-148">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a3adf-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="a3adf-149">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a3adf-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
