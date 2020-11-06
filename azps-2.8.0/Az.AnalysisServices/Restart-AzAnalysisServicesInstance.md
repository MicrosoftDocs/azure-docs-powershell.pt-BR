---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 623b7c84b29e5e64a47beeff6c9f7dba88edf32b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598161"
---
# <span data-ttu-id="74123-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="74123-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="74123-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74123-102">SYNOPSIS</span></span>
<span data-ttu-id="74123-103">Reinicia uma instância do servidor do Analysis Services no ambiente atualmente conectado, conforme especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="74123-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="74123-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74123-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74123-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74123-105">DESCRIPTION</span></span>
<span data-ttu-id="74123-106">O cmdlet Restart-AzAnalysisServicesInstance reinicia uma instância do servidor do Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="74123-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="74123-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74123-107">EXAMPLES</span></span>

### <span data-ttu-id="74123-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="74123-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="74123-109">Esse comando irá reiniciar o servidor ' TestServer ' no ambiente especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="74123-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="74123-110">OS</span><span class="sxs-lookup"><span data-stu-id="74123-110">PARAMETERS</span></span>

### <span data-ttu-id="74123-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="74123-111">-Instance</span></span>
<span data-ttu-id="74123-112">Nome da instância do servidor do Analysis Services para reiniciar</span><span class="sxs-lookup"><span data-stu-id="74123-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74123-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74123-113">-PassThru</span></span>
<span data-ttu-id="74123-114">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="74123-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="74123-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74123-115">-Confirm</span></span>
<span data-ttu-id="74123-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74123-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74123-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74123-117">-WhatIf</span></span>
<span data-ttu-id="74123-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74123-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74123-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74123-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74123-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74123-120">CommonParameters</span></span>
<span data-ttu-id="74123-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74123-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74123-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74123-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74123-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74123-123">INPUTS</span></span>

### <span data-ttu-id="74123-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="74123-124">None</span></span>

## <span data-ttu-id="74123-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74123-125">OUTPUTS</span></span>

### <span data-ttu-id="74123-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74123-126">System.Boolean</span></span>

## <span data-ttu-id="74123-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74123-127">NOTES</span></span>
<span data-ttu-id="74123-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="74123-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="74123-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74123-129">RELATED LINKS</span></span>
