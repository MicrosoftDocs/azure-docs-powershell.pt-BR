---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 6a3dc975c34d4938235ce95743f73f833a948b49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887242"
---
# <span data-ttu-id="73846-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="73846-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="73846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73846-102">SYNOPSIS</span></span>
<span data-ttu-id="73846-103">Baixe e instale o kubectl, a ferramenta de linha de comando Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="73846-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="73846-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="73846-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73846-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="73846-105">DESCRIPTION</span></span>
<span data-ttu-id="73846-106">Baixe e instale o kubectl, a ferramenta de linha de comando Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="73846-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="73846-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73846-107">EXAMPLES</span></span>

### <span data-ttu-id="73846-108">Baixar e instalar a versão mais recente do kubectl</span><span class="sxs-lookup"><span data-stu-id="73846-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="73846-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="73846-109">PARAMETERS</span></span>

### <span data-ttu-id="73846-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73846-110">-AsJob</span></span>
<span data-ttu-id="73846-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="73846-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73846-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73846-112">-DefaultProfile</span></span>
<span data-ttu-id="73846-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73846-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73846-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="73846-114">-Destination</span></span>
<span data-ttu-id="73846-115">Caminho no qual instalar o kubectl.</span><span class="sxs-lookup"><span data-stu-id="73846-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="73846-116">Padrão para instalar em ~/.azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="73846-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="73846-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="73846-117">-DownloadFromMirror</span></span>
<span data-ttu-id="73846-118">Baixar do site espelho : https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="73846-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="73846-119">-Force</span><span class="sxs-lookup"><span data-stu-id="73846-119">-Force</span></span>
<span data-ttu-id="73846-120">Substituir kubectl existente sem prompt</span><span class="sxs-lookup"><span data-stu-id="73846-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="73846-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73846-121">-PassThru</span></span>
<span data-ttu-id="73846-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="73846-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="73846-123">-Version</span><span class="sxs-lookup"><span data-stu-id="73846-123">-Version</span></span>
<span data-ttu-id="73846-124">Versão do kubectl a ser instalada, por exemplo, 'v1.17.2'.</span><span class="sxs-lookup"><span data-stu-id="73846-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="73846-125">Valor padrão: Mais recente</span><span class="sxs-lookup"><span data-stu-id="73846-125">Default value: Latest</span></span>

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

### <span data-ttu-id="73846-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73846-126">-Confirm</span></span>
<span data-ttu-id="73846-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73846-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73846-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73846-128">-WhatIf</span></span>
<span data-ttu-id="73846-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73846-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73846-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73846-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73846-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73846-131">CommonParameters</span></span>
<span data-ttu-id="73846-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73846-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73846-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73846-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73846-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73846-134">INPUTS</span></span>

### <span data-ttu-id="73846-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="73846-135">None</span></span>

## <span data-ttu-id="73846-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="73846-136">OUTPUTS</span></span>

### <span data-ttu-id="73846-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73846-137">System.Boolean</span></span>

## <span data-ttu-id="73846-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="73846-138">NOTES</span></span>

## <span data-ttu-id="73846-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73846-139">RELATED LINKS</span></span>
