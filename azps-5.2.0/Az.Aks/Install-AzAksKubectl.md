---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261319"
---
# <span data-ttu-id="548fa-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="548fa-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="548fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="548fa-102">SYNOPSIS</span></span>
<span data-ttu-id="548fa-103">Baixar e instalar o kubectl, a ferramenta de linha de comando do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="548fa-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="548fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="548fa-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="548fa-105">DESCRIPTION</span></span>
<span data-ttu-id="548fa-106">Baixar e instalar o kubectl, a ferramenta de linha de comando do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="548fa-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="548fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="548fa-107">EXAMPLES</span></span>

### <span data-ttu-id="548fa-108">Baixar e instalar a versão mais recente do kubectl</span><span class="sxs-lookup"><span data-stu-id="548fa-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="548fa-109">OS</span><span class="sxs-lookup"><span data-stu-id="548fa-109">PARAMETERS</span></span>

### <span data-ttu-id="548fa-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="548fa-110">-AsJob</span></span>
<span data-ttu-id="548fa-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="548fa-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="548fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548fa-112">-DefaultProfile</span></span>
<span data-ttu-id="548fa-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="548fa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="548fa-114">-Destino</span><span class="sxs-lookup"><span data-stu-id="548fa-114">-Destination</span></span>
<span data-ttu-id="548fa-115">Caminho no qual instalar o kubectl.</span><span class="sxs-lookup"><span data-stu-id="548fa-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="548fa-116">Padrão para instalar em ~/.Azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="548fa-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="548fa-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="548fa-117">-DownloadFromMirror</span></span>
<span data-ttu-id="548fa-118">Download a partir do site de espelhamento: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="548fa-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="548fa-119">-Force</span><span class="sxs-lookup"><span data-stu-id="548fa-119">-Force</span></span>
<span data-ttu-id="548fa-120">Substituir kubectl existente sem aviso</span><span class="sxs-lookup"><span data-stu-id="548fa-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="548fa-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="548fa-121">-PassThru</span></span>
<span data-ttu-id="548fa-122">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="548fa-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="548fa-123">-Versão</span><span class="sxs-lookup"><span data-stu-id="548fa-123">-Version</span></span>
<span data-ttu-id="548fa-124">Versão do kubectl para instalar, por exemplo, ' v 1.17.2 '.</span><span class="sxs-lookup"><span data-stu-id="548fa-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="548fa-125">Valor padrão: mais recente</span><span class="sxs-lookup"><span data-stu-id="548fa-125">Default value: Latest</span></span>

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

### <span data-ttu-id="548fa-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="548fa-126">-Confirm</span></span>
<span data-ttu-id="548fa-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="548fa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548fa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548fa-128">-WhatIf</span></span>
<span data-ttu-id="548fa-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="548fa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548fa-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="548fa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548fa-131">CommonParameters</span></span>
<span data-ttu-id="548fa-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548fa-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="548fa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548fa-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="548fa-134">INPUTS</span></span>

### <span data-ttu-id="548fa-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="548fa-135">None</span></span>

## <span data-ttu-id="548fa-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="548fa-136">OUTPUTS</span></span>

### <span data-ttu-id="548fa-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="548fa-137">System.Boolean</span></span>

## <span data-ttu-id="548fa-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="548fa-138">NOTES</span></span>

## <span data-ttu-id="548fa-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="548fa-139">RELATED LINKS</span></span>
