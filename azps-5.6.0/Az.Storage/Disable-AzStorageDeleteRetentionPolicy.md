---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: dac884a0faf44380f19447f2d52af1e172feb9a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888060"
---
# <span data-ttu-id="8d0ce-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d0ce-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8d0ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="8d0ce-103">Desabilite a política de retenção de exclusão para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d0ce-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8d0ce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8d0ce-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d0ce-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8d0ce-105">DESCRIPTION</span></span>
<span data-ttu-id="8d0ce-106">O cmdlet **Disable-AzStorageDeleteRetentionPolicy** desabilita a política de retenção de exclusão para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d0ce-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8d0ce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d0ce-107">EXAMPLES</span></span>

### <span data-ttu-id="8d0ce-108">Exemplo 1: Desabilitar a política de retenção de exclusão para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="8d0ce-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="8d0ce-109">Este comando desabilita a política de retenção de exclusão para o serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="8d0ce-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="8d0ce-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8d0ce-110">PARAMETERS</span></span>

### <span data-ttu-id="8d0ce-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8d0ce-111">-Context</span></span>
<span data-ttu-id="8d0ce-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="8d0ce-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8d0ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d0ce-113">-DefaultProfile</span></span>
<span data-ttu-id="8d0ce-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d0ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d0ce-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d0ce-115">-PassThru</span></span>
<span data-ttu-id="8d0ce-116">Exibir DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="8d0ce-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="8d0ce-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d0ce-117">-Confirm</span></span>
<span data-ttu-id="8d0ce-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d0ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d0ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d0ce-119">-WhatIf</span></span>
<span data-ttu-id="8d0ce-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d0ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d0ce-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d0ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d0ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d0ce-122">CommonParameters</span></span>
<span data-ttu-id="8d0ce-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d0ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d0ce-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d0ce-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d0ce-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d0ce-125">INPUTS</span></span>

### <span data-ttu-id="8d0ce-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d0ce-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8d0ce-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8d0ce-127">OUTPUTS</span></span>

### <span data-ttu-id="8d0ce-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d0ce-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8d0ce-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="8d0ce-129">NOTES</span></span>

## <span data-ttu-id="8d0ce-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d0ce-130">RELATED LINKS</span></span>
