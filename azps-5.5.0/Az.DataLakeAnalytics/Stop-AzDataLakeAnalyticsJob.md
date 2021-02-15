---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115401"
---
# <span data-ttu-id="1a990-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1a990-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="1a990-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a990-102">SYNOPSIS</span></span>
<span data-ttu-id="1a990-103">Cancela um trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a990-103">Cancels a job.</span></span>

## <span data-ttu-id="1a990-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a990-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a990-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a990-105">DESCRIPTION</span></span>
<span data-ttu-id="1a990-106">O cmdlet **Stop-AzDataLakeAnalytics Job** cancela um trabalho do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1a990-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="1a990-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a990-107">EXAMPLES</span></span>

### <span data-ttu-id="1a990-108">Exemplo 1: Cancelar um trabalho</span><span class="sxs-lookup"><span data-stu-id="1a990-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="1a990-109">Esse comando cancela o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="1a990-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="1a990-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a990-110">PARAMETERS</span></span>

### <span data-ttu-id="1a990-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="1a990-111">-Account</span></span>
<span data-ttu-id="1a990-112">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1a990-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a990-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a990-113">-DefaultProfile</span></span>
<span data-ttu-id="1a990-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1a990-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a990-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1a990-115">-Force</span></span>
<span data-ttu-id="1a990-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1a990-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a990-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="1a990-117">-JobId</span></span>
<span data-ttu-id="1a990-118">Especifica a ID do trabalho a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="1a990-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a990-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a990-119">-PassThru</span></span>
<span data-ttu-id="1a990-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1a990-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1a990-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="1a990-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a990-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1a990-122">-Confirm</span></span>
<span data-ttu-id="1a990-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a990-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a990-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a990-124">-WhatIf</span></span>
<span data-ttu-id="1a990-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1a990-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a990-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a990-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a990-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a990-127">CommonParameters</span></span>
<span data-ttu-id="1a990-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a990-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a990-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a990-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a990-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="1a990-130">INPUTS</span></span>

### <span data-ttu-id="1a990-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1a990-131">System.String</span></span>

### <span data-ttu-id="1a990-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1a990-132">System.Guid</span></span>

### <span data-ttu-id="1a990-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1a990-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a990-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="1a990-134">OUTPUTS</span></span>

### <span data-ttu-id="1a990-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a990-135">System.Boolean</span></span>

## <span data-ttu-id="1a990-136">Notas</span><span class="sxs-lookup"><span data-stu-id="1a990-136">NOTES</span></span>

## <span data-ttu-id="1a990-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a990-137">RELATED LINKS</span></span>

[<span data-ttu-id="1a990-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1a990-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="1a990-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1a990-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="1a990-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1a990-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


