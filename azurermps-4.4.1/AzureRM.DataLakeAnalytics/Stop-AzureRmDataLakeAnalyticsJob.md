---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: a0848ffc888b4812a28198749417d0b0894a5d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610507"
---
# <span data-ttu-id="52808-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="52808-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="52808-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52808-102">SYNOPSIS</span></span>
<span data-ttu-id="52808-103">Cancela um trabalho.</span><span class="sxs-lookup"><span data-stu-id="52808-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52808-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52808-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52808-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52808-105">DESCRIPTION</span></span>
<span data-ttu-id="52808-106">O cmdlet **Stop-AzureRmDataLakeAnalyticsJob** cancela um trabalho do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="52808-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="52808-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52808-107">EXAMPLES</span></span>

### <span data-ttu-id="52808-108">Exemplo 1: cancelar um trabalho</span><span class="sxs-lookup"><span data-stu-id="52808-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="52808-109">Este comando cancela o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="52808-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="52808-110">OS</span><span class="sxs-lookup"><span data-stu-id="52808-110">PARAMETERS</span></span>

### <span data-ttu-id="52808-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="52808-111">-Account</span></span>
<span data-ttu-id="52808-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="52808-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="52808-113">-Force</span><span class="sxs-lookup"><span data-stu-id="52808-113">-Force</span></span>
<span data-ttu-id="52808-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="52808-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52808-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="52808-115">-JobId</span></span>
<span data-ttu-id="52808-116">Especifica a ID do trabalho a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="52808-116">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="52808-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52808-117">-PassThru</span></span>
<span data-ttu-id="52808-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="52808-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52808-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="52808-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52808-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52808-120">-Confirm</span></span>
<span data-ttu-id="52808-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52808-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52808-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52808-122">-WhatIf</span></span>
<span data-ttu-id="52808-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52808-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52808-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52808-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52808-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52808-125">-DefaultProfile</span></span>
<span data-ttu-id="52808-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52808-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52808-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52808-127">CommonParameters</span></span>
<span data-ttu-id="52808-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52808-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52808-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52808-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52808-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52808-130">INPUTS</span></span>

### <span data-ttu-id="52808-131">#C0</span><span class="sxs-lookup"><span data-stu-id="52808-131">Guid</span></span>
<span data-ttu-id="52808-132">O parâmetro ' JobId ' aceita o valor do tipo ' GUID ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="52808-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="52808-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52808-133">OUTPUTS</span></span>

### <span data-ttu-id="52808-134">bool</span><span class="sxs-lookup"><span data-stu-id="52808-134">bool</span></span>
<span data-ttu-id="52808-135">Se PassThru for especificado, retornará true após a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="52808-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="52808-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52808-136">NOTES</span></span>

## <span data-ttu-id="52808-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52808-137">RELATED LINKS</span></span>

[<span data-ttu-id="52808-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="52808-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="52808-139">Enviar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="52808-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="52808-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="52808-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


