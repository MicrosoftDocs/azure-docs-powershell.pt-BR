---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 45b8bc67529556e9a9d53bd3280c6475f0e60df1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118741"
---
# <span data-ttu-id="e4b37-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e4b37-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="e4b37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4b37-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b37-103">Registra um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4b37-103">Registers a resource provider.</span></span>

## <span data-ttu-id="e4b37-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4b37-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4b37-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4b37-105">DESCRIPTION</span></span>
<span data-ttu-id="e4b37-106">O cmdlet **Register-AzResourceProvider** registra um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4b37-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="e4b37-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4b37-107">EXAMPLES</span></span>

### <span data-ttu-id="e4b37-108">Exemplo 1: Registrar um provedor</span><span class="sxs-lookup"><span data-stu-id="e4b37-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="e4b37-109">Isso registrará o provedor microsoft.network da sua conta.</span><span class="sxs-lookup"><span data-stu-id="e4b37-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="e4b37-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4b37-110">PARAMETERS</span></span>

### <span data-ttu-id="e4b37-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e4b37-111">-ApiVersion</span></span>
<span data-ttu-id="e4b37-112">Especifica a versão da API com suporte do Provedor de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e4b37-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e4b37-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="e4b37-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e4b37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b37-114">-DefaultProfile</span></span>
<span data-ttu-id="e4b37-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e4b37-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4b37-116">-Pré-</span><span class="sxs-lookup"><span data-stu-id="e4b37-116">-Pre</span></span>
<span data-ttu-id="e4b37-117">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e4b37-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e4b37-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e4b37-118">-ProviderNamespace</span></span>
<span data-ttu-id="e4b37-119">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4b37-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="e4b37-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e4b37-120">-Confirm</span></span>
<span data-ttu-id="e4b37-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4b37-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4b37-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4b37-122">-WhatIf</span></span>
<span data-ttu-id="e4b37-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e4b37-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4b37-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4b37-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4b37-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b37-125">CommonParameters</span></span>
<span data-ttu-id="e4b37-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b37-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b37-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4b37-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b37-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4b37-128">INPUTS</span></span>

### <span data-ttu-id="e4b37-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e4b37-129">System.String</span></span>

## <span data-ttu-id="e4b37-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4b37-130">OUTPUTS</span></span>

### <span data-ttu-id="e4b37-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e4b37-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="e4b37-132">Notas</span><span class="sxs-lookup"><span data-stu-id="e4b37-132">NOTES</span></span>

## <span data-ttu-id="e4b37-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4b37-133">RELATED LINKS</span></span>

[<span data-ttu-id="e4b37-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e4b37-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="e4b37-135">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e4b37-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


