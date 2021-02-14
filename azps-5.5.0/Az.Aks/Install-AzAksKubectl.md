---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116680"
---
# <span data-ttu-id="b6128-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="b6128-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="b6128-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6128-102">SYNOPSIS</span></span>
<span data-ttu-id="b6128-103">Baixe e instale aectl, a ferramenta de linha de comando Desernetes.</span><span class="sxs-lookup"><span data-stu-id="b6128-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="b6128-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6128-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6128-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6128-105">DESCRIPTION</span></span>
<span data-ttu-id="b6128-106">Baixe e instale aectl, a ferramenta de linha de comando Desernetes.</span><span class="sxs-lookup"><span data-stu-id="b6128-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="b6128-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6128-107">EXAMPLES</span></span>

### <span data-ttu-id="b6128-108">Baixar e instalar a versão mais recente doectl</span><span class="sxs-lookup"><span data-stu-id="b6128-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="b6128-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6128-109">PARAMETERS</span></span>

### <span data-ttu-id="b6128-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6128-110">-AsJob</span></span>
<span data-ttu-id="b6128-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b6128-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6128-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6128-112">-DefaultProfile</span></span>
<span data-ttu-id="b6128-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6128-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6128-114">-Destino</span><span class="sxs-lookup"><span data-stu-id="b6128-114">-Destination</span></span>
<span data-ttu-id="b6128-115">Caminho no qual instalar oectl.</span><span class="sxs-lookup"><span data-stu-id="b6128-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="b6128-116">Padrão para instalar em ~/.azure-ectl/</span><span class="sxs-lookup"><span data-stu-id="b6128-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="b6128-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="b6128-117">-DownloadFromMirror</span></span>
<span data-ttu-id="b6128-118">Baixar do site espelhado: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="b6128-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="b6128-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b6128-119">-Force</span></span>
<span data-ttu-id="b6128-120">Substituir aectl existente sem aviso</span><span class="sxs-lookup"><span data-stu-id="b6128-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="b6128-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6128-121">-PassThru</span></span>
<span data-ttu-id="b6128-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b6128-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b6128-123">-Versão</span><span class="sxs-lookup"><span data-stu-id="b6128-123">-Version</span></span>
<span data-ttu-id="b6128-124">Versão deectl para instalação, por exemplo, 'v1.17.2'.</span><span class="sxs-lookup"><span data-stu-id="b6128-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="b6128-125">Valor padrão: Mais recente</span><span class="sxs-lookup"><span data-stu-id="b6128-125">Default value: Latest</span></span>

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

### <span data-ttu-id="b6128-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b6128-126">-Confirm</span></span>
<span data-ttu-id="b6128-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6128-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6128-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6128-128">-WhatIf</span></span>
<span data-ttu-id="b6128-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b6128-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6128-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6128-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6128-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6128-131">CommonParameters</span></span>
<span data-ttu-id="b6128-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6128-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6128-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6128-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6128-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="b6128-134">INPUTS</span></span>

### <span data-ttu-id="b6128-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b6128-135">None</span></span>

## <span data-ttu-id="b6128-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="b6128-136">OUTPUTS</span></span>

### <span data-ttu-id="b6128-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b6128-137">System.Boolean</span></span>

## <span data-ttu-id="b6128-138">Notas</span><span class="sxs-lookup"><span data-stu-id="b6128-138">NOTES</span></span>

## <span data-ttu-id="b6128-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6128-139">RELATED LINKS</span></span>
