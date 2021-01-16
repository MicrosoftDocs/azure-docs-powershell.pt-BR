---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262637"
---
# <span data-ttu-id="93350-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="93350-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="93350-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93350-102">SYNOPSIS</span></span>
<span data-ttu-id="93350-103">Obtém detalhes de uma política de backup de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="93350-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="93350-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93350-104">SYNTAX</span></span>

### <span data-ttu-id="93350-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="93350-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93350-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93350-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93350-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93350-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93350-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93350-108">DESCRIPTION</span></span>
<span data-ttu-id="93350-109">O cmdlet **Get-AzNetAppFilesBackupPolicy** Obtém detalhes de uma política de backup do ANF.</span><span class="sxs-lookup"><span data-stu-id="93350-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="93350-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93350-110">EXAMPLES</span></span>

### <span data-ttu-id="93350-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93350-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="93350-112">Esse comando obtém a política de backup chamada "MyBackupPolicy" para a conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="93350-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="93350-113">OS</span><span class="sxs-lookup"><span data-stu-id="93350-113">PARAMETERS</span></span>

### <span data-ttu-id="93350-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="93350-114">-AccountName</span></span>
<span data-ttu-id="93350-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="93350-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="93350-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="93350-116">-AccountObject</span></span>
<span data-ttu-id="93350-117">O objeto de conta que contém a política de backup a ser retornada</span><span class="sxs-lookup"><span data-stu-id="93350-117">The Account object containing the Backup Policy to return</span></span>

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

### <span data-ttu-id="93350-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93350-118">-DefaultProfile</span></span>
<span data-ttu-id="93350-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93350-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93350-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="93350-120">-Name</span></span>
<span data-ttu-id="93350-121">O nome da política de backup do ANF</span><span class="sxs-lookup"><span data-stu-id="93350-121">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="93350-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93350-122">-ResourceGroupName</span></span>
<span data-ttu-id="93350-123">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="93350-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="93350-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93350-124">-ResourceId</span></span>
<span data-ttu-id="93350-125">A ID do recurso da política de backup do ANF</span><span class="sxs-lookup"><span data-stu-id="93350-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="93350-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93350-126">CommonParameters</span></span>
<span data-ttu-id="93350-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93350-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93350-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93350-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93350-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93350-129">INPUTS</span></span>

### <span data-ttu-id="93350-130">System. String</span><span class="sxs-lookup"><span data-stu-id="93350-130">System.String</span></span>

### <span data-ttu-id="93350-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="93350-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="93350-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93350-132">OUTPUTS</span></span>

### <span data-ttu-id="93350-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="93350-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="93350-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93350-134">NOTES</span></span>

## <span data-ttu-id="93350-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93350-135">RELATED LINKS</span></span>
