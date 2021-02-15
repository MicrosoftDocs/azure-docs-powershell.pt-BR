---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112317"
---
# <span data-ttu-id="b00f7-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="b00f7-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="b00f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b00f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b00f7-103">Reinicia uma instância do servidor do Analysis Services no Ambiente conectado no momento, conforme especificado no Add-AzAnalysisServicesAccount comando</span><span class="sxs-lookup"><span data-stu-id="b00f7-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b00f7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b00f7-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b00f7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b00f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b00f7-106">O Restart-AzAnalysisServicesInstance cmdlet reinicia uma instância do servidor do Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b00f7-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="b00f7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b00f7-107">EXAMPLES</span></span>

### <span data-ttu-id="b00f7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b00f7-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="b00f7-109">Esse comando reiniciará o servidor "testserver" no ambiente especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b00f7-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b00f7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b00f7-110">PARAMETERS</span></span>

### <span data-ttu-id="b00f7-111">-Instância</span><span class="sxs-lookup"><span data-stu-id="b00f7-111">-Instance</span></span>
<span data-ttu-id="b00f7-112">Nome da instância do servidor do Analysis Services para reiniciar</span><span class="sxs-lookup"><span data-stu-id="b00f7-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="b00f7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b00f7-113">-PassThru</span></span>
<span data-ttu-id="b00f7-114">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b00f7-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b00f7-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b00f7-115">-Confirm</span></span>
<span data-ttu-id="b00f7-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b00f7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00f7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00f7-117">-WhatIf</span></span>
<span data-ttu-id="b00f7-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b00f7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00f7-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b00f7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00f7-120">CommonParameters</span></span>
<span data-ttu-id="b00f7-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00f7-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00f7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00f7-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="b00f7-123">INPUTS</span></span>

### <span data-ttu-id="b00f7-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b00f7-124">None</span></span>

## <span data-ttu-id="b00f7-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="b00f7-125">OUTPUTS</span></span>

### <span data-ttu-id="b00f7-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b00f7-126">System.Boolean</span></span>

## <span data-ttu-id="b00f7-127">Notas</span><span class="sxs-lookup"><span data-stu-id="b00f7-127">NOTES</span></span>
<span data-ttu-id="b00f7-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="b00f7-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="b00f7-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b00f7-129">RELATED LINKS</span></span>
