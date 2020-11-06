---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 496c0410808604303ab60d8ad4d989e838828bf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427373"
---
# <span data-ttu-id="ac976-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="ac976-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="ac976-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac976-102">SYNOPSIS</span></span>
<span data-ttu-id="ac976-103">Reinicia uma instância do servidor do Analysis Services no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ac976-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac976-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac976-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance -Instance <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac976-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac976-105">DESCRIPTION</span></span>
<span data-ttu-id="ac976-106">O cmdlet Restart-AzureAnalysisServicesInstance reinicia uma instância do servidor do Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ac976-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="ac976-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac976-107">EXAMPLES</span></span>

### <span data-ttu-id="ac976-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac976-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="ac976-109">Esse comando irá reiniciar o servidor ' TestServer ' no ambiente especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ac976-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="ac976-110">OS</span><span class="sxs-lookup"><span data-stu-id="ac976-110">PARAMETERS</span></span>

### <span data-ttu-id="ac976-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="ac976-111">-Instance</span></span>
<span data-ttu-id="ac976-112">Nome da instância do servidor do Analysis Services para reiniciar</span><span class="sxs-lookup"><span data-stu-id="ac976-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac976-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac976-113">-PassThru</span></span>
<span data-ttu-id="ac976-114">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ac976-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ac976-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ac976-115">-Confirm</span></span>
<span data-ttu-id="ac976-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac976-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac976-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac976-117">-WhatIf</span></span>
<span data-ttu-id="ac976-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac976-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac976-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac976-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac976-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac976-120">CommonParameters</span></span>
<span data-ttu-id="ac976-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac976-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac976-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac976-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac976-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac976-123">INPUTS</span></span>

### <span data-ttu-id="ac976-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ac976-124">None</span></span>

## <span data-ttu-id="ac976-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac976-125">OUTPUTS</span></span>

### <span data-ttu-id="ac976-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac976-126">System.Boolean</span></span>

## <span data-ttu-id="ac976-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac976-127">NOTES</span></span>
<span data-ttu-id="ac976-128">Alias: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="ac976-128">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="ac976-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac976-129">RELATED LINKS</span></span>
