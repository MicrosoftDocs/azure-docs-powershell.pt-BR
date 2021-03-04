---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: d37a717ba87771310de4f1944e3865712e00554e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889692"
---
# <span data-ttu-id="97123-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="97123-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="97123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97123-102">SYNOPSIS</span></span>
<span data-ttu-id="97123-103">Criar um objeto na memória para Extension</span><span class="sxs-lookup"><span data-stu-id="97123-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="97123-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="97123-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="97123-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="97123-105">DESCRIPTION</span></span>
<span data-ttu-id="97123-106">Criar um objeto na memória para Extension</span><span class="sxs-lookup"><span data-stu-id="97123-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="97123-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97123-107">EXAMPLES</span></span>

### <span data-ttu-id="97123-108">Exemplo 1: Criar objeto de extensão de Geneva</span><span class="sxs-lookup"><span data-stu-id="97123-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="97123-109">Este comando cria um objeto de extensão geneva que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="97123-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="97123-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="97123-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="97123-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="97123-111">PARAMETERS</span></span>

### <span data-ttu-id="97123-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="97123-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="97123-113">Especifique explicitamente se o CRP pode atualizar automaticamente typeHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="97123-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97123-114">-Name</span><span class="sxs-lookup"><span data-stu-id="97123-114">-Name</span></span>
<span data-ttu-id="97123-115">Nome.</span><span class="sxs-lookup"><span data-stu-id="97123-115">Name.</span></span>

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

### <span data-ttu-id="97123-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="97123-116">-ProtectedSetting</span></span>
<span data-ttu-id="97123-117">Configurações protegidas para a extensão que são criptografadas antes de enviar para a VM.</span><span class="sxs-lookup"><span data-stu-id="97123-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

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

### <span data-ttu-id="97123-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="97123-118">-Publisher</span></span>
<span data-ttu-id="97123-119">Publisher.</span><span class="sxs-lookup"><span data-stu-id="97123-119">Publisher.</span></span>

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

### <span data-ttu-id="97123-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="97123-120">-RolesAppliedTo</span></span>
<span data-ttu-id="97123-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="97123-121">RolesAppliedTo.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97123-122">-Setting</span><span class="sxs-lookup"><span data-stu-id="97123-122">-Setting</span></span>
<span data-ttu-id="97123-123">Configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="97123-123">Public settings for the extension.</span></span>

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

### <span data-ttu-id="97123-124">-Type</span><span class="sxs-lookup"><span data-stu-id="97123-124">-Type</span></span>
<span data-ttu-id="97123-125">Digite.</span><span class="sxs-lookup"><span data-stu-id="97123-125">Type.</span></span>

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

### <span data-ttu-id="97123-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="97123-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="97123-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="97123-127">TypeHandlerVersion.</span></span>

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

### <span data-ttu-id="97123-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97123-128">CommonParameters</span></span>
<span data-ttu-id="97123-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97123-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97123-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97123-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97123-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97123-131">INPUTS</span></span>

## <span data-ttu-id="97123-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="97123-132">OUTPUTS</span></span>

### <span data-ttu-id="97123-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="97123-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="97123-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="97123-134">NOTES</span></span>

<span data-ttu-id="97123-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="97123-135">ALIASES</span></span>

## <span data-ttu-id="97123-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97123-136">RELATED LINKS</span></span>

