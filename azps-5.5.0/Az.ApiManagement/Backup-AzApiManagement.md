---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113659"
---
# <span data-ttu-id="dd0a7-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd0a7-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="dd0a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0a7-103">Fazer o back up de um serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="dd0a7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd0a7-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd0a7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd0a7-105">DESCRIPTION</span></span>
<span data-ttu-id="dd0a7-106">O **cmdlet Backup-AzApiManagement** backup de uma instância de um serviço de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="dd0a7-107">Este cmdlet armazena o backup como um blob de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="dd0a7-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dd0a7-108">EXAMPLES</span></span>

### <span data-ttu-id="dd0a7-109">Exemplo 1: Fazer o back up de um serviço de Gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="dd0a7-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="dd0a7-110">Esse comando fazer o back up de um serviço de Gerenciamento de API em um blob de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="dd0a7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd0a7-111">PARAMETERS</span></span>

### <span data-ttu-id="dd0a7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0a7-112">-DefaultProfile</span></span>
<span data-ttu-id="dd0a7-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd0a7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd0a7-114">-Name</span></span>
<span data-ttu-id="dd0a7-115">Especifica o nome da implantação de Gerenciamento de API que este cmdlet fazer o back-up.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="dd0a7-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd0a7-116">-PassThru</span></span>
<span data-ttu-id="dd0a7-117">Indica que esse cmdlet retorna o objeto **PsApiManagement** com backup, se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="dd0a7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd0a7-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd0a7-119">Especifica o nome do grupo de recursos no qual existe a implantação de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="dd0a7-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="dd0a7-120">-StorageContext</span></span>
<span data-ttu-id="dd0a7-121">Especifica um contexto de conexão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd0a7-122">-TargetBname</span><span class="sxs-lookup"><span data-stu-id="dd0a7-122">-TargetBlobName</span></span>
<span data-ttu-id="dd0a7-123">Especifica o nome do blob para o backup.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="dd0a7-124">Se o blob não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="dd0a7-125">Este cmdlet gera um valor padrão com base no seguinte padrão: {Name}-{yyyyy-MM-dd-HH-mm}.apimbackup</span><span class="sxs-lookup"><span data-stu-id="dd0a7-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0a7-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="dd0a7-126">-TargetContainerName</span></span>
<span data-ttu-id="dd0a7-127">Especifica o nome do contêiner do blob para o backup.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="dd0a7-128">Se o contêiner não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-128">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0a7-129">CommonParameters</span></span>
<span data-ttu-id="dd0a7-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd0a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0a7-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd0a7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0a7-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="dd0a7-132">INPUTS</span></span>

### <span data-ttu-id="dd0a7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dd0a7-133">System.String</span></span>

### <span data-ttu-id="dd0a7-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd0a7-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dd0a7-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="dd0a7-135">OUTPUTS</span></span>

### <span data-ttu-id="dd0a7-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd0a7-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="dd0a7-137">Notas</span><span class="sxs-lookup"><span data-stu-id="dd0a7-137">NOTES</span></span>

## <span data-ttu-id="dd0a7-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd0a7-138">RELATED LINKS</span></span>

[<span data-ttu-id="dd0a7-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd0a7-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="dd0a7-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd0a7-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="dd0a7-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd0a7-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="dd0a7-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd0a7-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


