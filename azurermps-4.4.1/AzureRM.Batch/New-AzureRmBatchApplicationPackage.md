---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: a67113443702d443bfd0b936af05e14c8fbbb96e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428280"
---
# <span data-ttu-id="15148-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15148-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="15148-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15148-102">SYNOPSIS</span></span>
<span data-ttu-id="15148-103">Cria um pacote de aplicativo em uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="15148-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15148-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15148-104">SYNTAX</span></span>

### <span data-ttu-id="15148-105">UploadAndActivate (padrão)</span><span class="sxs-lookup"><span data-stu-id="15148-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15148-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="15148-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15148-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15148-107">DESCRIPTION</span></span>
<span data-ttu-id="15148-108">O cmdlet **New-AzureRmBatchApplicationPackage** cria um pacote de aplicativo em uma conta de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="15148-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="15148-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15148-109">EXAMPLES</span></span>

### <span data-ttu-id="15148-110">Exemplo 1: instalar um pacote de aplicativo em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="15148-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="15148-111">Esse comando cria e ativa a versão 1,0 do aplicativo Litware e carrega o conteúdo de litware.1.0.zip como o conteúdo do pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15148-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="15148-112">OS</span><span class="sxs-lookup"><span data-stu-id="15148-112">PARAMETERS</span></span>

### <span data-ttu-id="15148-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15148-113">-AccountName</span></span>
<span data-ttu-id="15148-114">Especifica o nome da conta em lotes para a qual esse cmdlet adiciona um pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15148-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="15148-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="15148-115">-ActivateOnly</span></span>
<span data-ttu-id="15148-116">Indica que esse cmdlet ativa um pacote de aplicativo que já foi carregado.</span><span class="sxs-lookup"><span data-stu-id="15148-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="15148-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="15148-117">-ApplicationId</span></span>
<span data-ttu-id="15148-118">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15148-118">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="15148-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="15148-119">-ApplicationVersion</span></span>
<span data-ttu-id="15148-120">Especifica a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15148-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="15148-121">-FilePath</span><span class="sxs-lookup"><span data-stu-id="15148-121">-FilePath</span></span>
<span data-ttu-id="15148-122">Especifica o arquivo a ser carregado como o arquivo binário do pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="15148-122">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="15148-123">-Format</span><span class="sxs-lookup"><span data-stu-id="15148-123">-Format</span></span>
<span data-ttu-id="15148-124">Especifica o formato do arquivo binário do pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15148-124">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="15148-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15148-125">-ResourceGroupName</span></span>
<span data-ttu-id="15148-126">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="15148-126">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="15148-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15148-127">-DefaultProfile</span></span>
<span data-ttu-id="15148-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15148-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15148-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15148-129">CommonParameters</span></span>
<span data-ttu-id="15148-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15148-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15148-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15148-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15148-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15148-132">INPUTS</span></span>

## <span data-ttu-id="15148-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15148-133">OUTPUTS</span></span>

### <span data-ttu-id="15148-134">Microsoft.Azure.Commands.Batch. Modelos. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15148-134">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="15148-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15148-135">NOTES</span></span>

## <span data-ttu-id="15148-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15148-136">RELATED LINKS</span></span>

[<span data-ttu-id="15148-137">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15148-137">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="15148-138">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15148-138">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="15148-139">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15148-139">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="15148-140">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15148-140">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="15148-141">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15148-141">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="15148-142">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15148-142">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)

