---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: 761d34b4ed2d061b773c136a7d4e2db9f05a9103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115501"
---
# <span data-ttu-id="a35bb-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="a35bb-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="a35bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a35bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a35bb-103">Criar um objeto na memória para Extensão</span><span class="sxs-lookup"><span data-stu-id="a35bb-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="a35bb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a35bb-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="a35bb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a35bb-105">DESCRIPTION</span></span>
<span data-ttu-id="a35bb-106">Criar um objeto na memória para Extensão</span><span class="sxs-lookup"><span data-stu-id="a35bb-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="a35bb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a35bb-107">EXAMPLES</span></span>

### <span data-ttu-id="a35bb-108">Exemplo 1: Criar objeto de extensão de Extensão Desv.</span><span class="sxs-lookup"><span data-stu-id="a35bb-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="a35bb-109">Esse comando cria um objeto de extensão Desvões que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="a35bb-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="a35bb-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="a35bb-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="a35bb-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a35bb-111">PARAMETERS</span></span>

### <span data-ttu-id="a35bb-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a35bb-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a35bb-113">Especifique explicitamente se o CRP pode atualizar automaticamente o tipoHandlerVersion para versões secundárias mais altas quando eles se tornam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a35bb-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

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

### <span data-ttu-id="a35bb-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a35bb-114">-Name</span></span>
<span data-ttu-id="a35bb-115">Nome.</span><span class="sxs-lookup"><span data-stu-id="a35bb-115">Name.</span></span>

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

### <span data-ttu-id="a35bb-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="a35bb-116">-ProtectedSetting</span></span>
<span data-ttu-id="a35bb-117">Configurações protegidas para a extensão que são criptografadas antes de enviadas para o VM.</span><span class="sxs-lookup"><span data-stu-id="a35bb-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

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

### <span data-ttu-id="a35bb-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a35bb-118">-Publisher</span></span>
<span data-ttu-id="a35bb-119">Editor.</span><span class="sxs-lookup"><span data-stu-id="a35bb-119">Publisher.</span></span>

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

### <span data-ttu-id="a35bb-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="a35bb-120">-RolesAppliedTo</span></span>
<span data-ttu-id="a35bb-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="a35bb-121">RolesAppliedTo.</span></span>

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

### <span data-ttu-id="a35bb-122">-Configuração</span><span class="sxs-lookup"><span data-stu-id="a35bb-122">-Setting</span></span>
<span data-ttu-id="a35bb-123">Configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="a35bb-123">Public settings for the extension.</span></span>

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

### <span data-ttu-id="a35bb-124">-Tipo</span><span class="sxs-lookup"><span data-stu-id="a35bb-124">-Type</span></span>
<span data-ttu-id="a35bb-125">Tipo.</span><span class="sxs-lookup"><span data-stu-id="a35bb-125">Type.</span></span>

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

### <span data-ttu-id="a35bb-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a35bb-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="a35bb-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="a35bb-127">TypeHandlerVersion.</span></span>

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

### <span data-ttu-id="a35bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35bb-128">CommonParameters</span></span>
<span data-ttu-id="a35bb-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a35bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35bb-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a35bb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35bb-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="a35bb-131">INPUTS</span></span>

## <span data-ttu-id="a35bb-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="a35bb-132">OUTPUTS</span></span>

### <span data-ttu-id="a35bb-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="a35bb-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="a35bb-134">Notas</span><span class="sxs-lookup"><span data-stu-id="a35bb-134">NOTES</span></span>

<span data-ttu-id="a35bb-135">Aliases</span><span class="sxs-lookup"><span data-stu-id="a35bb-135">ALIASES</span></span>

## <span data-ttu-id="a35bb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a35bb-136">RELATED LINKS</span></span>

