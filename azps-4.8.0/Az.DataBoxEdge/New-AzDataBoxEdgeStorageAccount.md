---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 2a5a1314f422a7b91a5cc8885abe0af98fa395a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112549"
---
# <span data-ttu-id="98a08-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98a08-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="98a08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98a08-102">SYNOPSIS</span></span>
<span data-ttu-id="98a08-103">Cria uma nova conta de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98a08-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="98a08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98a08-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98a08-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98a08-105">DESCRIPTION</span></span>
<span data-ttu-id="98a08-106">O cmdlet **New-AzDataBoxEdgeStorageAccount** cria uma nova conta de armazenamento de borda em um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="98a08-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="98a08-107">Para um dispositivo, uma conta de armazenamento de borda pode ser mapeada no máximo para apenas uma conta de armazenamento em nuvem.</span><span class="sxs-lookup"><span data-stu-id="98a08-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="98a08-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98a08-108">EXAMPLES</span></span>

### <span data-ttu-id="98a08-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98a08-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="98a08-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="98a08-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="98a08-111">2 EdgeStorageAccounts no dispositivo não pode compartilhar mais do que uma conta de armazenamento em nuvem</span><span class="sxs-lookup"><span data-stu-id="98a08-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="98a08-112">OS</span><span class="sxs-lookup"><span data-stu-id="98a08-112">PARAMETERS</span></span>

### <span data-ttu-id="98a08-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98a08-113">-AsJob</span></span>
<span data-ttu-id="98a08-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="98a08-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98a08-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="98a08-115">-Cloud</span></span>
<span data-ttu-id="98a08-116">Usará um CloudStorageAccount para hierarquização</span><span class="sxs-lookup"><span data-stu-id="98a08-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="98a08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a08-117">-DefaultProfile</span></span>
<span data-ttu-id="98a08-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98a08-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98a08-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="98a08-119">-DeviceName</span></span>
<span data-ttu-id="98a08-120">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="98a08-120">Device Name</span></span>

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

### <span data-ttu-id="98a08-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="98a08-121">-Name</span></span>
<span data-ttu-id="98a08-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="98a08-122">Resource Name</span></span>

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

### <span data-ttu-id="98a08-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a08-123">-ResourceGroupName</span></span>
<span data-ttu-id="98a08-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="98a08-124">Resource Group Name</span></span>

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

### <span data-ttu-id="98a08-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="98a08-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="98a08-126">Fornecer o nome do recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="98a08-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="98a08-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98a08-127">-Confirm</span></span>
<span data-ttu-id="98a08-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98a08-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98a08-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98a08-129">-WhatIf</span></span>
<span data-ttu-id="98a08-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98a08-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98a08-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98a08-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98a08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a08-132">CommonParameters</span></span>
<span data-ttu-id="98a08-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a08-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98a08-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a08-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98a08-135">INPUTS</span></span>

### <span data-ttu-id="98a08-136">System. String</span><span class="sxs-lookup"><span data-stu-id="98a08-136">System.String</span></span>

### <span data-ttu-id="98a08-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98a08-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98a08-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98a08-138">OUTPUTS</span></span>

### <span data-ttu-id="98a08-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98a08-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="98a08-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98a08-140">NOTES</span></span>

## <span data-ttu-id="98a08-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98a08-141">RELATED LINKS</span></span>
