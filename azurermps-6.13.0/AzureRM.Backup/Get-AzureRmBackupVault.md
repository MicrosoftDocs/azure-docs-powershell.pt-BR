---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: c11170e6bee80b9eaa19135ad604d8bf70e1baab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609417"
---
# <span data-ttu-id="003e0-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="003e0-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="003e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="003e0-102">SYNOPSIS</span></span>
<span data-ttu-id="003e0-103">Obtém cofres de backup.</span><span class="sxs-lookup"><span data-stu-id="003e0-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="003e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="003e0-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="003e0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="003e0-105">DESCRIPTION</span></span>
<span data-ttu-id="003e0-106">O cmdlet **Get-AzureRmBackupVault** Obtém cofres de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="003e0-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="003e0-107">Esse cmdlet retorna objetos **AzureRmBackupVault** para uso com outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="003e0-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="003e0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="003e0-108">EXAMPLES</span></span>

### <span data-ttu-id="003e0-109">Exemplo 1: exibir todos os cofres de backup</span><span class="sxs-lookup"><span data-stu-id="003e0-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="003e0-110">Esse comando obtém todos os cofres de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="003e0-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="003e0-111">Exemplo 2: exibir todos os cofres criados no oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="003e0-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="003e0-112">Esse comando obtém todos os cofres de backup.</span><span class="sxs-lookup"><span data-stu-id="003e0-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="003e0-113">O comando passa a ele para o cmdlet Where-Object usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="003e0-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="003e0-114">Esse cmdlet filtra os resultados com base na propriedade **Region** .</span><span class="sxs-lookup"><span data-stu-id="003e0-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="003e0-115">Para obter mais informações, digite `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="003e0-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="003e0-116">Exemplo 3: obter um cofre específico</span><span class="sxs-lookup"><span data-stu-id="003e0-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="003e0-117">Esse comando obtém o cofre chamado Vault03.</span><span class="sxs-lookup"><span data-stu-id="003e0-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="003e0-118">Exemplo 4: contar o número de cofres que têm armazenamento redundante localmente</span><span class="sxs-lookup"><span data-stu-id="003e0-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="003e0-119">Esse comando obtém todos os cofres de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="003e0-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="003e0-120">O comando passa essas pessoas para **Where-Object** , que filtra os resultados com base na propriedade **Storage** .</span><span class="sxs-lookup"><span data-stu-id="003e0-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="003e0-121">O comando passa aqueles que têm um valor de LocallyRedundant para o cmdlet Measure-Object, que conta os resultados.</span><span class="sxs-lookup"><span data-stu-id="003e0-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="003e0-122">Para obter mais informações, digite `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="003e0-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="003e0-123">OS</span><span class="sxs-lookup"><span data-stu-id="003e0-123">PARAMETERS</span></span>

### <span data-ttu-id="003e0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003e0-124">-DefaultProfile</span></span>
<span data-ttu-id="003e0-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="003e0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="003e0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="003e0-126">-Name</span></span>
<span data-ttu-id="003e0-127">Especifica o nome do cofre de backup que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="003e0-127">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="003e0-128">Se mais de um cofre de backup tiver o mesmo nome, esse cmdlet retornará todos eles.</span><span class="sxs-lookup"><span data-stu-id="003e0-128">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="003e0-129">Especifique o parâmetro *ResourceGroupName* para obter um cofre exclusivo.</span><span class="sxs-lookup"><span data-stu-id="003e0-129">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

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

### <span data-ttu-id="003e0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003e0-130">-ResourceGroupName</span></span>
<span data-ttu-id="003e0-131">Especifica o nome de um grupo de recursos do Azure em que esse cmdlet obtém um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="003e0-131">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

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

### <span data-ttu-id="003e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003e0-132">CommonParameters</span></span>
<span data-ttu-id="003e0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="003e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003e0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="003e0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003e0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="003e0-135">INPUTS</span></span>

### <span data-ttu-id="003e0-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="003e0-136">None</span></span>

## <span data-ttu-id="003e0-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="003e0-137">OUTPUTS</span></span>

### <span data-ttu-id="003e0-138">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="003e0-138">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="003e0-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="003e0-139">NOTES</span></span>

## <span data-ttu-id="003e0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="003e0-140">RELATED LINKS</span></span>

[<span data-ttu-id="003e0-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="003e0-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="003e0-142">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="003e0-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="003e0-143">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="003e0-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="003e0-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="003e0-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


