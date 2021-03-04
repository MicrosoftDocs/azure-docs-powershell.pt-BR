---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: fc8e3d49f5c5a6430a6436b0d46e8fd10984db98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887464"
---
# <span data-ttu-id="17961-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="17961-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="17961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17961-102">SYNOPSIS</span></span>
<span data-ttu-id="17961-103">Obtém detalhes de uma Política de Backup de Arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="17961-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="17961-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17961-104">SYNTAX</span></span>

### <span data-ttu-id="17961-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17961-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17961-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17961-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17961-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17961-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17961-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17961-108">DESCRIPTION</span></span>
<span data-ttu-id="17961-109">O cmdlet **Get-AzNetAppFilesBackupPolicy** obtém detalhes de uma política de backup ANF.</span><span class="sxs-lookup"><span data-stu-id="17961-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="17961-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17961-110">EXAMPLES</span></span>

### <span data-ttu-id="17961-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17961-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="17961-112">Este comando obtém a política de backup chamada "MyBackupPolicy" para a conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="17961-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="17961-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17961-113">PARAMETERS</span></span>

### <span data-ttu-id="17961-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="17961-114">-AccountName</span></span>
<span data-ttu-id="17961-115">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="17961-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17961-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="17961-116">-AccountObject</span></span>
<span data-ttu-id="17961-117">O objeto Account que contém a Política de Backup a ser retornada</span><span class="sxs-lookup"><span data-stu-id="17961-117">The Account object containing the Backup Policy to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17961-118">-DefaultProfile</span></span>
<span data-ttu-id="17961-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17961-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17961-120">-Name</span><span class="sxs-lookup"><span data-stu-id="17961-120">-Name</span></span>
<span data-ttu-id="17961-121">O nome da política de backup da ANF</span><span class="sxs-lookup"><span data-stu-id="17961-121">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17961-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17961-122">-ResourceGroupName</span></span>
<span data-ttu-id="17961-123">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="17961-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17961-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17961-124">-ResourceId</span></span>
<span data-ttu-id="17961-125">A id de recurso da Política de Backup da ANF</span><span class="sxs-lookup"><span data-stu-id="17961-125">The resource id of the ANF Backup Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17961-126">CommonParameters</span></span>
<span data-ttu-id="17961-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17961-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17961-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17961-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17961-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17961-129">INPUTS</span></span>

### <span data-ttu-id="17961-130">System.String</span><span class="sxs-lookup"><span data-stu-id="17961-130">System.String</span></span>

### <span data-ttu-id="17961-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="17961-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="17961-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17961-132">OUTPUTS</span></span>

### <span data-ttu-id="17961-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="17961-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="17961-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="17961-134">NOTES</span></span>

## <span data-ttu-id="17961-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17961-135">RELATED LINKS</span></span>
