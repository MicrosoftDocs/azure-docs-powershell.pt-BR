---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 4fc5c20cf43fbafb89007328307c69d4820b2127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602962"
---
# <span data-ttu-id="17959-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="17959-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="17959-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17959-102">SYNOPSIS</span></span>
<span data-ttu-id="17959-103">Cancela um trabalho.</span><span class="sxs-lookup"><span data-stu-id="17959-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17959-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17959-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17959-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17959-105">DESCRIPTION</span></span>
<span data-ttu-id="17959-106">O cmdlet **Stop-AzureRmDataLakeAnalyticsJob** cancela um trabalho do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="17959-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="17959-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17959-107">EXAMPLES</span></span>

### <span data-ttu-id="17959-108">Exemplo 1: cancelar um trabalho</span><span class="sxs-lookup"><span data-stu-id="17959-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="17959-109">Este comando cancela o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="17959-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="17959-110">OS</span><span class="sxs-lookup"><span data-stu-id="17959-110">PARAMETERS</span></span>

### <span data-ttu-id="17959-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="17959-111">-Account</span></span>
<span data-ttu-id="17959-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="17959-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="17959-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17959-113">-DefaultProfile</span></span>
<span data-ttu-id="17959-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="17959-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17959-115">-Force</span><span class="sxs-lookup"><span data-stu-id="17959-115">-Force</span></span>
<span data-ttu-id="17959-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="17959-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17959-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="17959-117">-JobId</span></span>
<span data-ttu-id="17959-118">Especifica a ID do trabalho a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="17959-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="17959-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17959-119">-PassThru</span></span>
<span data-ttu-id="17959-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="17959-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="17959-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="17959-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17959-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17959-122">-Confirm</span></span>
<span data-ttu-id="17959-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17959-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17959-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17959-124">-WhatIf</span></span>
<span data-ttu-id="17959-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17959-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17959-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17959-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17959-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17959-127">CommonParameters</span></span>
<span data-ttu-id="17959-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17959-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17959-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17959-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17959-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17959-130">INPUTS</span></span>

### <span data-ttu-id="17959-131">System. String</span><span class="sxs-lookup"><span data-stu-id="17959-131">System.String</span></span>

### <span data-ttu-id="17959-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="17959-132">System.Guid</span></span>

### <span data-ttu-id="17959-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="17959-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="17959-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17959-134">OUTPUTS</span></span>

### <span data-ttu-id="17959-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17959-135">System.Boolean</span></span>

## <span data-ttu-id="17959-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17959-136">NOTES</span></span>

## <span data-ttu-id="17959-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17959-137">RELATED LINKS</span></span>

[<span data-ttu-id="17959-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="17959-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="17959-139">Enviar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="17959-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="17959-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="17959-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


