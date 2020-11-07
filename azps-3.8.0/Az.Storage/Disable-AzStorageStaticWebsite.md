---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941253"
---
# <span data-ttu-id="e4a05-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e4a05-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="e4a05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4a05-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a05-103">Desative o site estático para a conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4a05-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="e4a05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4a05-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4a05-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4a05-105">DESCRIPTION</span></span>
<span data-ttu-id="e4a05-106">O cmdlet **Disable-AzStorageStaticWebsite** desabilita o site estático para a conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4a05-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="e4a05-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4a05-107">EXAMPLES</span></span>

### <span data-ttu-id="e4a05-108">Exemplo 1: desabilitar o site estático para uma conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="e4a05-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="e4a05-109">Esse comando desabilita o site estático para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4a05-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="e4a05-110">OS</span><span class="sxs-lookup"><span data-stu-id="e4a05-110">PARAMETERS</span></span>

### <span data-ttu-id="e4a05-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e4a05-111">-Context</span></span>
<span data-ttu-id="e4a05-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="e4a05-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e4a05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a05-113">-DefaultProfile</span></span>
<span data-ttu-id="e4a05-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4a05-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4a05-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4a05-115">-PassThru</span></span>
<span data-ttu-id="e4a05-116">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="e4a05-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e4a05-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4a05-117">-Confirm</span></span>
<span data-ttu-id="e4a05-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4a05-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4a05-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4a05-119">-WhatIf</span></span>
<span data-ttu-id="e4a05-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4a05-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4a05-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4a05-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4a05-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a05-122">CommonParameters</span></span>
<span data-ttu-id="e4a05-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4a05-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a05-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4a05-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a05-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4a05-125">INPUTS</span></span>

### <span data-ttu-id="e4a05-126">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e4a05-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e4a05-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4a05-127">OUTPUTS</span></span>

### <span data-ttu-id="e4a05-128">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="e4a05-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="e4a05-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4a05-129">NOTES</span></span>

## <span data-ttu-id="e4a05-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4a05-130">RELATED LINKS</span></span>
