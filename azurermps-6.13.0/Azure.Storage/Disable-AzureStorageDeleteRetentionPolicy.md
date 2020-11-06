---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 656fe09054b1cfae90175cc4ea55370f80dfd8e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427370"
---
# <span data-ttu-id="16c3a-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="16c3a-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="16c3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="16c3a-103">Desabilite a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="16c3a-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16c3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16c3a-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16c3a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="16c3a-106">O cmdlet **Disable-AzureStorageDeleteRetentionPolicy** desabilita a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="16c3a-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="16c3a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16c3a-107">EXAMPLES</span></span>

### <span data-ttu-id="16c3a-108">Exemplo 1: desabilitar a política de retenção de exclusão para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="16c3a-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="16c3a-109">Este comando desabilita a política de retenção de exclusão do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="16c3a-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="16c3a-110">OS</span><span class="sxs-lookup"><span data-stu-id="16c3a-110">PARAMETERS</span></span>

### <span data-ttu-id="16c3a-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="16c3a-111">-Context</span></span>
<span data-ttu-id="16c3a-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="16c3a-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="16c3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c3a-113">-DefaultProfile</span></span>
<span data-ttu-id="16c3a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16c3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c3a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16c3a-115">-PassThru</span></span>
<span data-ttu-id="16c3a-116">Exibir DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="16c3a-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="16c3a-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16c3a-117">-Confirm</span></span>
<span data-ttu-id="16c3a-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16c3a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c3a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c3a-119">-WhatIf</span></span>
<span data-ttu-id="16c3a-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16c3a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c3a-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16c3a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c3a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c3a-122">CommonParameters</span></span>
<span data-ttu-id="16c3a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c3a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c3a-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c3a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c3a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16c3a-125">INPUTS</span></span>

### <span data-ttu-id="16c3a-126">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="16c3a-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="16c3a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16c3a-127">OUTPUTS</span></span>

### <span data-ttu-id="16c3a-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="16c3a-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="16c3a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16c3a-129">NOTES</span></span>

## <span data-ttu-id="16c3a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16c3a-130">RELATED LINKS</span></span>
