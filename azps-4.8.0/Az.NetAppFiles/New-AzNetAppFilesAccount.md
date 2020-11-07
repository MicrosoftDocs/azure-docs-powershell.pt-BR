---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955478"
---
# <span data-ttu-id="85109-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="85109-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="85109-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85109-102">SYNOPSIS</span></span>
<span data-ttu-id="85109-103">Cria uma nova conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="85109-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="85109-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85109-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85109-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85109-105">DESCRIPTION</span></span>
<span data-ttu-id="85109-106">O cmdlet **New-AzNetAppFilesAccount** cria uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="85109-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="85109-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85109-107">EXAMPLES</span></span>

### <span data-ttu-id="85109-108">Exemplo 1: criar uma conta do ANF</span><span class="sxs-lookup"><span data-stu-id="85109-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="85109-109">Esse comando cria a nova conta do ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="85109-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="85109-110">OS</span><span class="sxs-lookup"><span data-stu-id="85109-110">PARAMETERS</span></span>

### <span data-ttu-id="85109-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="85109-111">-ActiveDirectory</span></span>
<span data-ttu-id="85109-112">Uma matriz de Hashtable que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="85109-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="85109-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85109-113">-DefaultProfile</span></span>
<span data-ttu-id="85109-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85109-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85109-115">-Local</span><span class="sxs-lookup"><span data-stu-id="85109-115">-Location</span></span>
<span data-ttu-id="85109-116">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="85109-116">The location of the resource</span></span>

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

### <span data-ttu-id="85109-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="85109-117">-Name</span></span>
<span data-ttu-id="85109-118">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="85109-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="85109-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85109-119">-ResourceGroupName</span></span>
<span data-ttu-id="85109-120">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="85109-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="85109-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="85109-121">-Tag</span></span>
<span data-ttu-id="85109-122">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="85109-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="85109-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85109-123">-Confirm</span></span>
<span data-ttu-id="85109-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85109-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85109-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85109-125">-WhatIf</span></span>
<span data-ttu-id="85109-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85109-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85109-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85109-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85109-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85109-128">CommonParameters</span></span>
<span data-ttu-id="85109-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85109-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85109-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85109-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85109-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85109-131">INPUTS</span></span>

### <span data-ttu-id="85109-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="85109-132">None</span></span>

## <span data-ttu-id="85109-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85109-133">OUTPUTS</span></span>

### <span data-ttu-id="85109-134">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="85109-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="85109-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85109-135">NOTES</span></span>

## <span data-ttu-id="85109-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85109-136">RELATED LINKS</span></span>
