---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271338"
---
# <span data-ttu-id="cf677-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cf677-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="cf677-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf677-102">SYNOPSIS</span></span>
<span data-ttu-id="cf677-103">Habilite o site estático para a conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf677-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="cf677-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf677-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf677-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf677-105">DESCRIPTION</span></span>
<span data-ttu-id="cf677-106">O cmdlet **Enable-AzStorageStaticWebsite** habilita o site estático para a conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf677-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="cf677-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf677-107">EXAMPLES</span></span>

### <span data-ttu-id="cf677-108">Exemplo 1: habilitar o site estático para a conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="cf677-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="cf677-109">Esse comando habilita o site estático para a conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf677-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="cf677-110">OS</span><span class="sxs-lookup"><span data-stu-id="cf677-110">PARAMETERS</span></span>

### <span data-ttu-id="cf677-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cf677-111">-Context</span></span>
<span data-ttu-id="cf677-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="cf677-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="cf677-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf677-113">-DefaultProfile</span></span>
<span data-ttu-id="cf677-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf677-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf677-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="cf677-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="cf677-116">O caminho para o documento de erro que deve ser mostrado quando um 404 é emitido (ou seja, quando um navegador solicita uma página que não existe.)</span><span class="sxs-lookup"><span data-stu-id="cf677-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf677-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="cf677-117">-IndexDocument</span></span>
<span data-ttu-id="cf677-118">O nome do documento de índice em cada diretório.</span><span class="sxs-lookup"><span data-stu-id="cf677-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf677-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf677-119">-PassThru</span></span>
<span data-ttu-id="cf677-120">Exiba a configuração estática de site em Serviceproperties.</span><span class="sxs-lookup"><span data-stu-id="cf677-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="cf677-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf677-121">-Confirm</span></span>
<span data-ttu-id="cf677-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf677-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf677-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf677-123">-WhatIf</span></span>
<span data-ttu-id="cf677-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf677-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf677-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf677-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf677-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf677-126">CommonParameters</span></span>
<span data-ttu-id="cf677-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf677-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf677-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf677-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf677-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf677-129">INPUTS</span></span>

### <span data-ttu-id="cf677-130">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cf677-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cf677-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf677-131">OUTPUTS</span></span>

### <span data-ttu-id="cf677-132">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="cf677-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="cf677-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf677-133">NOTES</span></span>

## <span data-ttu-id="cf677-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf677-134">RELATED LINKS</span></span>
