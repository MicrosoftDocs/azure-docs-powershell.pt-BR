---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111389"
---
# <span data-ttu-id="ed928-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ed928-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="ed928-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed928-102">SYNOPSIS</span></span>
<span data-ttu-id="ed928-103">Não conta com um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed928-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="ed928-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed928-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed928-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed928-105">DESCRIPTION</span></span>
<span data-ttu-id="ed928-106">O **cmdlet Unregister-AzResourceProvider** não registrou um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed928-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="ed928-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed928-107">EXAMPLES</span></span>

### <span data-ttu-id="ed928-108">Exemplo 1: Provedor de recursos não-registro com ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ed928-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="ed928-109">Este comando desosterna o provedor de recursos "Microsoft.support".</span><span class="sxs-lookup"><span data-stu-id="ed928-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="ed928-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed928-110">PARAMETERS</span></span>

### <span data-ttu-id="ed928-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ed928-111">-ApiVersion</span></span>
<span data-ttu-id="ed928-112">Especifica a versão da API com suporte do Provedor de Recursos.</span><span class="sxs-lookup"><span data-stu-id="ed928-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ed928-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="ed928-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed928-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed928-114">-DefaultProfile</span></span>
<span data-ttu-id="ed928-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ed928-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed928-116">-Pré-</span><span class="sxs-lookup"><span data-stu-id="ed928-116">-Pre</span></span>
<span data-ttu-id="ed928-117">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="ed928-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ed928-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ed928-118">-ProviderNamespace</span></span>
<span data-ttu-id="ed928-119">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed928-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="ed928-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ed928-120">-Confirm</span></span>
<span data-ttu-id="ed928-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed928-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed928-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed928-122">-WhatIf</span></span>
<span data-ttu-id="ed928-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ed928-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed928-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed928-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed928-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed928-125">CommonParameters</span></span>
<span data-ttu-id="ed928-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed928-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed928-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed928-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed928-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="ed928-128">INPUTS</span></span>

### <span data-ttu-id="ed928-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ed928-129">System.String</span></span>

## <span data-ttu-id="ed928-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="ed928-130">OUTPUTS</span></span>

### <span data-ttu-id="ed928-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ed928-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="ed928-132">Notas</span><span class="sxs-lookup"><span data-stu-id="ed928-132">NOTES</span></span>

## <span data-ttu-id="ed928-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed928-133">RELATED LINKS</span></span>

[<span data-ttu-id="ed928-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ed928-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="ed928-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ed928-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


