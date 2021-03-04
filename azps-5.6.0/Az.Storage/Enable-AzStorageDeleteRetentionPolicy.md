---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 1d55c52b3c022e9e935051cdb1ad23aae32eecbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888055"
---
# <span data-ttu-id="c1a9d-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1a9d-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c1a9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a9d-103">Habilitar a política de retenção de exclusão para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a9d-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c1a9d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c1a9d-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1a9d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c1a9d-105">DESCRIPTION</span></span>
<span data-ttu-id="c1a9d-106">O cmdlet **Enable-AzStorageDeleteRetentionPolicy** permite excluir política de retenção para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a9d-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c1a9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1a9d-107">EXAMPLES</span></span>

### <span data-ttu-id="c1a9d-108">Exemplo 1: Habilitar a política de retenção de exclusão para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="c1a9d-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="c1a9d-109">Esse comando permite excluir a política de retenção para o serviço Blob e definir os dias de retenção de blob excluídos como 3.</span><span class="sxs-lookup"><span data-stu-id="c1a9d-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="c1a9d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c1a9d-110">PARAMETERS</span></span>

### <span data-ttu-id="c1a9d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c1a9d-111">-Context</span></span>
<span data-ttu-id="c1a9d-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="c1a9d-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a9d-113">-DefaultProfile</span></span>
<span data-ttu-id="c1a9d-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1a9d-115">-PassThru</span></span>
<span data-ttu-id="c1a9d-116">Exibir DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="c1a9d-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="c1a9d-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c1a9d-117">-RetentionDays</span></span>
<span data-ttu-id="c1a9d-118">Define o número de dias de retenção para DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="c1a9d-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1a9d-119">-Confirm</span></span>
<span data-ttu-id="c1a9d-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1a9d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1a9d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1a9d-121">-WhatIf</span></span>
<span data-ttu-id="c1a9d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1a9d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1a9d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1a9d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1a9d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a9d-124">CommonParameters</span></span>
<span data-ttu-id="c1a9d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a9d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a9d-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1a9d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a9d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1a9d-127">INPUTS</span></span>

### <span data-ttu-id="c1a9d-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c1a9d-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c1a9d-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c1a9d-129">OUTPUTS</span></span>

### <span data-ttu-id="c1a9d-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1a9d-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c1a9d-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="c1a9d-131">NOTES</span></span>

## <span data-ttu-id="c1a9d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1a9d-132">RELATED LINKS</span></span>
