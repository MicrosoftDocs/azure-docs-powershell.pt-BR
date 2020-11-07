---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 36176b16fab75b24549ceeb3d107114632703129
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941251"
---
# <span data-ttu-id="c89c5-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c89c5-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c89c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c89c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c89c5-103">Habilite a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c89c5-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c89c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c89c5-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c89c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c89c5-105">DESCRIPTION</span></span>
<span data-ttu-id="c89c5-106">O cmdlet **Enable-AzStorageDeleteRetentionPolicy** permite excluir a política de retenção para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c89c5-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c89c5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c89c5-107">EXAMPLES</span></span>

### <span data-ttu-id="c89c5-108">Exemplo 1: habilitar a política de retenção de exclusão para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="c89c5-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="c89c5-109">Esse comando habilita a política de retenção de exclusão para o serviço BLOB e define os dias de retenção de blob excluídos como 3.</span><span class="sxs-lookup"><span data-stu-id="c89c5-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="c89c5-110">OS</span><span class="sxs-lookup"><span data-stu-id="c89c5-110">PARAMETERS</span></span>

### <span data-ttu-id="c89c5-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c89c5-111">-Context</span></span>
<span data-ttu-id="c89c5-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="c89c5-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="c89c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c89c5-113">-DefaultProfile</span></span>
<span data-ttu-id="c89c5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c89c5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c89c5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c89c5-115">-PassThru</span></span>
<span data-ttu-id="c89c5-116">Exibir DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="c89c5-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="c89c5-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c89c5-117">-RetentionDays</span></span>
<span data-ttu-id="c89c5-118">Define o número de dias de retenção para o DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="c89c5-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="c89c5-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c89c5-119">-Confirm</span></span>
<span data-ttu-id="c89c5-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c89c5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c89c5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c89c5-121">-WhatIf</span></span>
<span data-ttu-id="c89c5-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c89c5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c89c5-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c89c5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c89c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c89c5-124">CommonParameters</span></span>
<span data-ttu-id="c89c5-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c89c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c89c5-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c89c5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c89c5-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c89c5-127">INPUTS</span></span>

### <span data-ttu-id="c89c5-128">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c89c5-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c89c5-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c89c5-129">OUTPUTS</span></span>

### <span data-ttu-id="c89c5-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c89c5-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c89c5-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c89c5-131">NOTES</span></span>

## <span data-ttu-id="c89c5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c89c5-132">RELATED LINKS</span></span>
