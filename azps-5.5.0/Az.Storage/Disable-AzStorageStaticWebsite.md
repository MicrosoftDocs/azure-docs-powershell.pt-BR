---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113678"
---
# <span data-ttu-id="bc571-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bc571-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="bc571-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc571-102">SYNOPSIS</span></span>
<span data-ttu-id="bc571-103">Desabilitar o site estático para a conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc571-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="bc571-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc571-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc571-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc571-105">DESCRIPTION</span></span>
<span data-ttu-id="bc571-106">O cmdlet **Disable-AzStorageWebWebsite** desabilita o site estático para a conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc571-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="bc571-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc571-107">EXAMPLES</span></span>

### <span data-ttu-id="bc571-108">Exemplo 1: Desabilitar o site estático para uma conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="bc571-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="bc571-109">Esse comando desabilita o site estático para uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc571-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="bc571-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc571-110">PARAMETERS</span></span>

### <span data-ttu-id="bc571-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bc571-111">-Context</span></span>
<span data-ttu-id="bc571-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="bc571-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="bc571-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc571-113">-DefaultProfile</span></span>
<span data-ttu-id="bc571-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc571-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc571-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc571-115">-PassThru</span></span>
<span data-ttu-id="bc571-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bc571-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bc571-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bc571-117">-Confirm</span></span>
<span data-ttu-id="bc571-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc571-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc571-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc571-119">-WhatIf</span></span>
<span data-ttu-id="bc571-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bc571-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc571-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc571-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc571-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc571-122">CommonParameters</span></span>
<span data-ttu-id="bc571-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc571-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc571-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc571-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc571-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="bc571-125">INPUTS</span></span>

### <span data-ttu-id="bc571-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bc571-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bc571-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="bc571-127">OUTPUTS</span></span>

### <span data-ttu-id="bc571-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="bc571-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="bc571-129">Notas</span><span class="sxs-lookup"><span data-stu-id="bc571-129">NOTES</span></span>

## <span data-ttu-id="bc571-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc571-130">RELATED LINKS</span></span>
