---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 3858c2ad6ca90716d5c9140949a683b9c409a105
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901495"
---
# <span data-ttu-id="ebf2d-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ebf2d-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="ebf2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebf2d-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf2d-103">Cancela um trabalho.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-103">Cancels a job.</span></span>

## <span data-ttu-id="ebf2d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ebf2d-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebf2d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ebf2d-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf2d-106">O cmdlet **Stop-AzDataLakeAnalyticsJob** cancela um trabalho do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="ebf2d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ebf2d-107">EXAMPLES</span></span>

### <span data-ttu-id="ebf2d-108">Exemplo 1: Cancelar um trabalho</span><span class="sxs-lookup"><span data-stu-id="ebf2d-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="ebf2d-109">Esse comando cancela o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="ebf2d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ebf2d-110">PARAMETERS</span></span>

### <span data-ttu-id="ebf2d-111">-Account</span><span class="sxs-lookup"><span data-stu-id="ebf2d-111">-Account</span></span>
<span data-ttu-id="ebf2d-112">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ebf2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf2d-113">-DefaultProfile</span></span>
<span data-ttu-id="ebf2d-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ebf2d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebf2d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ebf2d-115">-Force</span></span>
<span data-ttu-id="ebf2d-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ebf2d-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="ebf2d-117">-JobId</span></span>
<span data-ttu-id="ebf2d-118">Especifica a ID do trabalho a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="ebf2d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebf2d-119">-PassThru</span></span>
<span data-ttu-id="ebf2d-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ebf2d-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ebf2d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebf2d-122">-Confirm</span></span>
<span data-ttu-id="ebf2d-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebf2d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf2d-124">-WhatIf</span></span>
<span data-ttu-id="ebf2d-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebf2d-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebf2d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf2d-127">CommonParameters</span></span>
<span data-ttu-id="ebf2d-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf2d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf2d-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebf2d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf2d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebf2d-130">INPUTS</span></span>

### <span data-ttu-id="ebf2d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ebf2d-131">System.String</span></span>

### <span data-ttu-id="ebf2d-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ebf2d-132">System.Guid</span></span>

### <span data-ttu-id="ebf2d-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ebf2d-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ebf2d-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ebf2d-134">OUTPUTS</span></span>

### <span data-ttu-id="ebf2d-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebf2d-135">System.Boolean</span></span>

## <span data-ttu-id="ebf2d-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ebf2d-136">NOTES</span></span>

## <span data-ttu-id="ebf2d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebf2d-137">RELATED LINKS</span></span>

[<span data-ttu-id="ebf2d-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ebf2d-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ebf2d-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ebf2d-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ebf2d-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ebf2d-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


