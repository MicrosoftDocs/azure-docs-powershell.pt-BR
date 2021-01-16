---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262626"
---
# <span data-ttu-id="54e39-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="54e39-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="54e39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54e39-102">SYNOPSIS</span></span>
<span data-ttu-id="54e39-103">Cria uma nova conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="54e39-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="54e39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54e39-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e39-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54e39-105">DESCRIPTION</span></span>
<span data-ttu-id="54e39-106">O cmdlet **New-AzNetAppFilesAccount** cria uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="54e39-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="54e39-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54e39-107">EXAMPLES</span></span>

### <span data-ttu-id="54e39-108">Exemplo 1: criar uma conta do ANF</span><span class="sxs-lookup"><span data-stu-id="54e39-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="54e39-109">Esse comando cria a nova conta do ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="54e39-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="54e39-110">OS</span><span class="sxs-lookup"><span data-stu-id="54e39-110">PARAMETERS</span></span>

### <span data-ttu-id="54e39-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="54e39-111">-ActiveDirectory</span></span>
<span data-ttu-id="54e39-112">Uma matriz de Hashtable que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="54e39-112">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e39-113">-DefaultProfile</span></span>
<span data-ttu-id="54e39-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54e39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54e39-115">-Local</span><span class="sxs-lookup"><span data-stu-id="54e39-115">-Location</span></span>
<span data-ttu-id="54e39-116">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="54e39-116">The location of the resource</span></span>

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

### <span data-ttu-id="54e39-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="54e39-117">-Name</span></span>
<span data-ttu-id="54e39-118">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="54e39-118">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e39-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e39-119">-ResourceGroupName</span></span>
<span data-ttu-id="54e39-120">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="54e39-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="54e39-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="54e39-121">-Tag</span></span>
<span data-ttu-id="54e39-122">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="54e39-122">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e39-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54e39-123">-Confirm</span></span>
<span data-ttu-id="54e39-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54e39-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e39-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e39-125">-WhatIf</span></span>
<span data-ttu-id="54e39-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54e39-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e39-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54e39-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e39-128">CommonParameters</span></span>
<span data-ttu-id="54e39-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e39-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54e39-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e39-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54e39-131">INPUTS</span></span>

### <span data-ttu-id="54e39-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="54e39-132">None</span></span>

## <span data-ttu-id="54e39-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54e39-133">OUTPUTS</span></span>

### <span data-ttu-id="54e39-134">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="54e39-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="54e39-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54e39-135">NOTES</span></span>

## <span data-ttu-id="54e39-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54e39-136">RELATED LINKS</span></span>
