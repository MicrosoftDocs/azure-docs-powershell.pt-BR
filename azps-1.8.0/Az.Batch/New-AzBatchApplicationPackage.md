---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: 0e5494506873917be7897c547eca900174f5bcab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601462"
---
# <span data-ttu-id="d2e54-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e54-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="d2e54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2e54-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e54-103">Cria um pacote de aplicativo em uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="d2e54-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="d2e54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2e54-104">SYNTAX</span></span>

### <span data-ttu-id="d2e54-105">UploadAndActivate (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2e54-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e54-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="d2e54-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2e54-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2e54-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e54-108">O cmdlet **New-AzBatchApplicationPackage** cria um pacote de aplicativo em uma conta de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e54-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="d2e54-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2e54-109">EXAMPLES</span></span>

### <span data-ttu-id="d2e54-110">Exemplo 1: instalar um pacote de aplicativo em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="d2e54-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="d2e54-111">Esse comando cria e ativa a versão 1,0 do aplicativo Litware e carrega o conteúdo de litware.1.0.zip como o conteúdo do pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2e54-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="d2e54-112">OS</span><span class="sxs-lookup"><span data-stu-id="d2e54-112">PARAMETERS</span></span>

### <span data-ttu-id="d2e54-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2e54-113">-AccountName</span></span>
<span data-ttu-id="d2e54-114">Especifica o nome da conta em lotes para a qual esse cmdlet adiciona um pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2e54-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="d2e54-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="d2e54-115">-ActivateOnly</span></span>
<span data-ttu-id="d2e54-116">Indica que esse cmdlet ativa um pacote de aplicativo que já foi carregado.</span><span class="sxs-lookup"><span data-stu-id="d2e54-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e54-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d2e54-117">-ApplicationId</span></span>
<span data-ttu-id="d2e54-118">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2e54-118">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e54-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="d2e54-119">-ApplicationVersion</span></span>
<span data-ttu-id="d2e54-120">Especifica a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2e54-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e54-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e54-121">-DefaultProfile</span></span>
<span data-ttu-id="d2e54-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e54-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2e54-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d2e54-123">-FilePath</span></span>
<span data-ttu-id="d2e54-124">Especifica o arquivo a ser carregado como o arquivo binário do pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d2e54-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e54-125">-Format</span><span class="sxs-lookup"><span data-stu-id="d2e54-125">-Format</span></span>
<span data-ttu-id="d2e54-126">Especifica o formato do arquivo binário do pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2e54-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e54-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2e54-128">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="d2e54-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d2e54-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e54-129">CommonParameters</span></span>
<span data-ttu-id="d2e54-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e54-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e54-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e54-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e54-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2e54-132">INPUTS</span></span>

### <span data-ttu-id="d2e54-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e54-133">System.String</span></span>

### <span data-ttu-id="d2e54-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d2e54-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d2e54-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2e54-135">OUTPUTS</span></span>

### <span data-ttu-id="d2e54-136">Microsoft.Azure.Commands.Batch. Modelos. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e54-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="d2e54-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2e54-137">NOTES</span></span>

## <span data-ttu-id="d2e54-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2e54-138">RELATED LINKS</span></span>

[<span data-ttu-id="d2e54-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e54-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="d2e54-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e54-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="d2e54-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e54-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="d2e54-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e54-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="d2e54-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e54-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="d2e54-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e54-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


