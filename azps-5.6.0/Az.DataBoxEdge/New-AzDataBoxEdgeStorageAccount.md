---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: c0cea590ced7abdaad1021453304ea1508790b55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888711"
---
# <span data-ttu-id="21f59-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21f59-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="21f59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21f59-102">SYNOPSIS</span></span>
<span data-ttu-id="21f59-103">Cria uma nova conta de Armazenamento de Borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="21f59-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="21f59-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="21f59-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21f59-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="21f59-105">DESCRIPTION</span></span>
<span data-ttu-id="21f59-106">O cmdlet **New-AzDataBoxEdgeStorageAccount** cria uma nova conta de Armazenamento de Borda em um dispositivo de Borda de Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="21f59-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="21f59-107">Para um dispositivo, uma conta de Armazenamento de Borda pode ser mapeada no máximo para apenas uma conta de Armazenamento na Nuvem.</span><span class="sxs-lookup"><span data-stu-id="21f59-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="21f59-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21f59-108">EXAMPLES</span></span>

### <span data-ttu-id="21f59-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21f59-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="21f59-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="21f59-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="21f59-111">2 EdgeStorageAccounts no dispositivo não pode compartilhar mais de 1 conta de armazenamento na nuvem</span><span class="sxs-lookup"><span data-stu-id="21f59-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="21f59-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="21f59-112">PARAMETERS</span></span>

### <span data-ttu-id="21f59-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21f59-113">-AsJob</span></span>
<span data-ttu-id="21f59-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="21f59-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21f59-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="21f59-115">-Cloud</span></span>
<span data-ttu-id="21f59-116">Usará um CloudStorageAccount para camadas</span><span class="sxs-lookup"><span data-stu-id="21f59-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f59-117">-DefaultProfile</span></span>
<span data-ttu-id="21f59-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21f59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f59-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="21f59-119">-DeviceName</span></span>
<span data-ttu-id="21f59-120">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="21f59-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f59-121">-Name</span><span class="sxs-lookup"><span data-stu-id="21f59-121">-Name</span></span>
<span data-ttu-id="21f59-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="21f59-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f59-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f59-123">-ResourceGroupName</span></span>
<span data-ttu-id="21f59-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="21f59-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f59-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="21f59-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="21f59-126">Fornecer o Nome de Recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="21f59-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f59-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21f59-127">-Confirm</span></span>
<span data-ttu-id="21f59-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f59-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21f59-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f59-129">-WhatIf</span></span>
<span data-ttu-id="21f59-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21f59-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21f59-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21f59-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21f59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f59-132">CommonParameters</span></span>
<span data-ttu-id="21f59-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21f59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f59-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21f59-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f59-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21f59-135">INPUTS</span></span>

### <span data-ttu-id="21f59-136">System.String</span><span class="sxs-lookup"><span data-stu-id="21f59-136">System.String</span></span>

### <span data-ttu-id="21f59-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="21f59-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="21f59-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="21f59-138">OUTPUTS</span></span>

### <span data-ttu-id="21f59-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21f59-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="21f59-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="21f59-140">NOTES</span></span>

## <span data-ttu-id="21f59-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21f59-141">RELATED LINKS</span></span>
