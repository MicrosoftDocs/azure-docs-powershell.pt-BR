---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 12881d387d1e98bef8ca1fa00790b0332a338b7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888059"
---
# <span data-ttu-id="fc2e7-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fc2e7-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="fc2e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="fc2e7-103">Desabilite o site estático para a conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc2e7-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="fc2e7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fc2e7-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc2e7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fc2e7-105">DESCRIPTION</span></span>
<span data-ttu-id="fc2e7-106">O cmdlet **Disable-AzStorageStaticWebsite** desabilita o site estático para a conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc2e7-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="fc2e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc2e7-107">EXAMPLES</span></span>

### <span data-ttu-id="fc2e7-108">Exemplo 1: Desabilitar o site estático para uma conta de Armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="fc2e7-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="fc2e7-109">Este comando desabilita o site estático para uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc2e7-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="fc2e7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fc2e7-110">PARAMETERS</span></span>

### <span data-ttu-id="fc2e7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fc2e7-111">-Context</span></span>
<span data-ttu-id="fc2e7-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="fc2e7-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="fc2e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc2e7-113">-DefaultProfile</span></span>
<span data-ttu-id="fc2e7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc2e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc2e7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc2e7-115">-PassThru</span></span>
<span data-ttu-id="fc2e7-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fc2e7-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fc2e7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc2e7-117">-Confirm</span></span>
<span data-ttu-id="fc2e7-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc2e7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc2e7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc2e7-119">-WhatIf</span></span>
<span data-ttu-id="fc2e7-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc2e7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc2e7-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc2e7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc2e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc2e7-122">CommonParameters</span></span>
<span data-ttu-id="fc2e7-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc2e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc2e7-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc2e7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc2e7-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc2e7-125">INPUTS</span></span>

### <span data-ttu-id="fc2e7-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fc2e7-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fc2e7-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fc2e7-127">OUTPUTS</span></span>

### <span data-ttu-id="fc2e7-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="fc2e7-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="fc2e7-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="fc2e7-129">NOTES</span></span>

## <span data-ttu-id="fc2e7-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc2e7-130">RELATED LINKS</span></span>
