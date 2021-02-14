---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 36176b16fab75b24549ceeb3d107114632703129
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115673"
---
# <span data-ttu-id="8f7c2-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8f7c2-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8f7c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7c2-103">Habilitar a política de retenção de exclusão para o serviço Blob de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8f7c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f7c2-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7c2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f7c2-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7c2-106">O cmdlet **Enable-AzStorageDeleteRetentionPolicy** habilita a política de retenção de exclusão para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8f7c2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f7c2-107">EXAMPLES</span></span>

### <span data-ttu-id="8f7c2-108">Exemplo 1: Habilitar a política de retenção de exclusão para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="8f7c2-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="8f7c2-109">Esse comando permite excluir a política de retenção do serviço Blob e definir os dias de retenção de blob excluídos como 3.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="8f7c2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f7c2-110">PARAMETERS</span></span>

### <span data-ttu-id="8f7c2-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8f7c2-111">-Context</span></span>
<span data-ttu-id="8f7c2-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="8f7c2-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8f7c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7c2-113">-DefaultProfile</span></span>
<span data-ttu-id="8f7c2-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f7c2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f7c2-115">-PassThru</span></span>
<span data-ttu-id="8f7c2-116">Exibir DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="8f7c2-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="8f7c2-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="8f7c2-117">-RetentionDays</span></span>
<span data-ttu-id="8f7c2-118">Define o número de dias de retenção para DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="8f7c2-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8f7c2-119">-Confirm</span></span>
<span data-ttu-id="8f7c2-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7c2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7c2-121">-WhatIf</span></span>
<span data-ttu-id="8f7c2-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7c2-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7c2-124">CommonParameters</span></span>
<span data-ttu-id="8f7c2-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7c2-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7c2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7c2-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f7c2-127">INPUTS</span></span>

### <span data-ttu-id="8f7c2-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8f7c2-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8f7c2-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f7c2-129">OUTPUTS</span></span>

### <span data-ttu-id="8f7c2-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8f7c2-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8f7c2-131">Notas</span><span class="sxs-lookup"><span data-stu-id="8f7c2-131">NOTES</span></span>

## <span data-ttu-id="8f7c2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f7c2-132">RELATED LINKS</span></span>
