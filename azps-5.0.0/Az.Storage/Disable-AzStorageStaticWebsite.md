---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125302"
---
# <span data-ttu-id="a57b5-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a57b5-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="a57b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a57b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a57b5-103">Desative o site estático para a conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a57b5-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="a57b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a57b5-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a57b5-105">DESCRIPTION</span></span>
<span data-ttu-id="a57b5-106">O cmdlet **Disable-AzStorageStaticWebsite** desabilita o site estático para a conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a57b5-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="a57b5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a57b5-107">EXAMPLES</span></span>

### <span data-ttu-id="a57b5-108">Exemplo 1: desabilitar o site estático para uma conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="a57b5-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="a57b5-109">Esse comando desabilita o site estático para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a57b5-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="a57b5-110">OS</span><span class="sxs-lookup"><span data-stu-id="a57b5-110">PARAMETERS</span></span>

### <span data-ttu-id="a57b5-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a57b5-111">-Context</span></span>
<span data-ttu-id="a57b5-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="a57b5-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="a57b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57b5-113">-DefaultProfile</span></span>
<span data-ttu-id="a57b5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a57b5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57b5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a57b5-115">-PassThru</span></span>
<span data-ttu-id="a57b5-116">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="a57b5-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a57b5-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a57b5-117">-Confirm</span></span>
<span data-ttu-id="a57b5-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a57b5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a57b5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57b5-119">-WhatIf</span></span>
<span data-ttu-id="a57b5-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a57b5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57b5-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a57b5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a57b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57b5-122">CommonParameters</span></span>
<span data-ttu-id="a57b5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57b5-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a57b5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57b5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a57b5-125">INPUTS</span></span>

### <span data-ttu-id="a57b5-126">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a57b5-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a57b5-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a57b5-127">OUTPUTS</span></span>

### <span data-ttu-id="a57b5-128">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="a57b5-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="a57b5-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a57b5-129">NOTES</span></span>

## <span data-ttu-id="a57b5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a57b5-130">RELATED LINKS</span></span>
