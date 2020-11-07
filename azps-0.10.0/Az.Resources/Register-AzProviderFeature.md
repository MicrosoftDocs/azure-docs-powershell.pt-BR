---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-Azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: b7c2be59ecf43c117a459d489af70dac7c836094
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776375"
---
# <span data-ttu-id="95f84-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="95f84-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="95f84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95f84-102">SYNOPSIS</span></span>
<span data-ttu-id="95f84-103">Registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="95f84-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="95f84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95f84-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95f84-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95f84-105">DESCRIPTION</span></span>
<span data-ttu-id="95f84-106">O cmdlet **Register-AzProviderFeature** registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="95f84-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="95f84-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95f84-107">EXAMPLES</span></span>

### <span data-ttu-id="95f84-108">Exemplo 1: registrar um recurso</span><span class="sxs-lookup"><span data-stu-id="95f84-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="95f84-109">Isso adiciona o recurso AllowApplicationSecurityGroups para a Microsoft. Network à sua conta.</span><span class="sxs-lookup"><span data-stu-id="95f84-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="95f84-110">OS</span><span class="sxs-lookup"><span data-stu-id="95f84-110">PARAMETERS</span></span>

### <span data-ttu-id="95f84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f84-111">-DefaultProfile</span></span>
<span data-ttu-id="95f84-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="95f84-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f84-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="95f84-113">-FeatureName</span></span>
<span data-ttu-id="95f84-114">Especifica o nome do recurso registrado por este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95f84-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="95f84-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="95f84-115">-ProviderNamespace</span></span>
<span data-ttu-id="95f84-116">Especifica um namespace para o qual esse cmdlet registra um recurso de provedor.</span><span class="sxs-lookup"><span data-stu-id="95f84-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="95f84-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95f84-117">-Confirm</span></span>
<span data-ttu-id="95f84-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95f84-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95f84-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95f84-119">-WhatIf</span></span>
<span data-ttu-id="95f84-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95f84-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95f84-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95f84-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95f84-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f84-122">CommonParameters</span></span>
<span data-ttu-id="95f84-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f84-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f84-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f84-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f84-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95f84-125">INPUTS</span></span>

## <span data-ttu-id="95f84-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95f84-126">OUTPUTS</span></span>

## <span data-ttu-id="95f84-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95f84-127">NOTES</span></span>

## <span data-ttu-id="95f84-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95f84-128">RELATED LINKS</span></span>

[<span data-ttu-id="95f84-129">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="95f84-129">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


